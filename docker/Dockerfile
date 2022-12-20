FROM nginx:latest

RUN env

RUN --mount=type=secret,id=mysecret,uid=0 cat /run/secrets/mysecret

RUN echo `ls /`
RUN echo `ls /run/`
RUN echo `ls /run/secrets/`
RUN TEST_ENV=$(cat /run/secrets/mysecret)
RUN echo ${TEST_ENV}
