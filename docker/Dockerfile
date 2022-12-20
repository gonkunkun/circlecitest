FROM nginx:latest

RUN env

# このマウントの仕方はOK. 多分ここで参照しないと揮発する。
RUN --mount=type=secret,id=mysecret,uid=0 cat /run/secrets/mysecret \
  TEST_ENV=$(cat /run/secrets/mysecret) && \
  echo `ls /` && \
  echo `ls /run/` && \
  echo `ls /run/secrets/`
RUN --mount=type=secret,id=mysecret2,uid=0 cat /run/secrets/mysecret2 \
  TEST_ENV=$(cat /run/secrets/mysecret2) && \
  echo `ls /` && \
  echo `ls /run/` && \
  echo `ls /run/secrets/`

RUN echo `ls /`
RUN echo `ls /run/`
RUN echo `ls /run/secrets/`
RUN TEST_ENV=$(cat /run/secrets/mysecret)
RUN echo ${TEST_ENV}
