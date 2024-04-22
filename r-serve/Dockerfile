FROM r-base:latest
RUN R -e "install.packages('Rserve', repos='http://cran.rstudio.com/')"
COPY server.crt /etc/ssl/certs/server.crt
COPY server.key /etc/ssl/private/server.key
COPY Rserve.conf /etc/Rserve.conf
CMD ["R", "CMD", "Rserve", "--vanilla", "--RS-conf", "/etc/Rserve.conf", "--RS-set", "daemon=disable" ]
#CMD ["R", "CMD", "Rserve", "--vanilla", "--RS-conf", "/etc/Rserve.conf", "--RS-set", "daemon=disable" ]
