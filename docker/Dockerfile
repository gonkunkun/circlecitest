FROM nginx:latest

RUN env

# このマウントの仕方はOK
RUN --mount=type=secret,id=mysecret,uid=0 cat /run/secrets/mysecret
RUN --mount=type=secret,id=mysecret2,uid=0 cat /run/secrets/mysecret2

RUN echo `ls -a /`
RUN echo `ls -a /run/`
RUN echo `ls -a /run/secrets/`
RUN TEST_ENV=$(cat /run/secrets/mysecret)
RUN echo ${TEST_ENV}
