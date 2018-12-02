FROM rocker/r-ver
RUN Rscript -e "install.packages('tidyverse')"
RUN Rscript -e 'install.packages("BiocManager"); BiocManager::install()'

COPY --from=continuumio/anaconda3 /opt/conda /opt/conda
ENV PATH /opt/conda/bin:$PATH
RUN Rscript -e "install.packages('IRkernel'); IRkernel::installspec()"

RUN mkdir -p /scratch && chmod a=rwx /scratch
WORKDIR /scratch

CMD ["jupyter", "notebook", "--no-browser", "--ip=0.0.0.0", "--allow-root"]
