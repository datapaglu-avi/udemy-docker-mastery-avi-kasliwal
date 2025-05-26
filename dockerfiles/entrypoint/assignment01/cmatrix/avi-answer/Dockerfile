FROM alpine:latest

RUN apk update \
    && apk upgrade \
    && apk add --no-cache cmatrix

ENTRYPOINT [ "cmatrix" ]

CMD ["-abs", "-C", "red"]

# Commands Ran to Build and Run the Docker Image

# docker image build -t datapagluavi/cmatrix:assignment_solve .
# ocker container run -it --rm --name cmatrix_ss datapagluavi/cmatrix:assignment_solve
# ocker container run -it --rm --name cmatrix_ss datapagluavi/cmatrix:assignment_solve -abs -C blue