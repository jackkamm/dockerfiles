FROM rocker/tidyverse

RUN apt-get install -y python3-pip
RUN pip3 install jupyter
RUN Rscript -e "install.packages('IRkernel')"
RUN Rscript -e "IRkernel::installspec()"

CMD ["jupyter", "notebook", "--no-browser", "--ip=0.0.0.0", "--allow-root"]
