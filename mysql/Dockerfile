FROM mysql

RUN groupadd -g 61000 webuser &&\
    useradd -g 61000 -l -M -s /bin/false -u 61000 webuser

USER webuser