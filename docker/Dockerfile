FROM nginx:latest

RUN env

RUN --mount=type=secret,id=mysecret,uid=0 cat /run/secrets/mysecret

RUN echo /run/secrets/mysecret
RUN echo ${TEST_ENV}
