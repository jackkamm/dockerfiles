FROM continuumio/anaconda3

FROM rocker/r-ver
RUN Rscript -e "install.packages('tidyverse')"
RUN Rscript -e 'install.packages("BiocManager"); BiocManager::install()'

COPY --from=0 /opt/conda /opt/conda
ENV PATH /opt/conda/bin:$PATH
RUN Rscript -e "install.packages('IRkernel')"
RUN Rscript -e "IRkernel::installspec()"
