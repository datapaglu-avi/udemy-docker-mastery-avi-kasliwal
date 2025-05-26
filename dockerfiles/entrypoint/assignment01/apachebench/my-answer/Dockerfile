FROM ubuntu:latest

RUN apt-get update \
    && apt-get install -y apache2-utils \
    && rm -rf /var/lib/apt/lists/*

ENTRYPOINT [ "ab" ]

CMD [ "-n", "10", "-c", "2", "https://lnmiit.ac.in/" ]

# docker image build -t datapagluavi/abtest:assignment_solve .
# docker container run -it --rm --name ab_lnmiit datapagluavi/abtest:assignment_solve --> 1362 ms
# docker container run -it --rm --name ab_lnmiit datapagluavi/abtest:assignment_solve -n 10 -c 2 https://blinkit.com/  --> 86 ms