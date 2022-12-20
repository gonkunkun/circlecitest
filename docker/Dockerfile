FROM nginx:latest

RUN env

# このマウントの仕方はOK. 多分ここで参照しないと揮発する。
RUN --mount=type=secret,id=mysecret,uid=0 \
  cat /run/secrets/mysecret && \
  TEST_ENV=$(cat /run/secrets/mysecret)

RUN --mount=type=secret,id=mysecret2,uid=0 \
  cat /run/secrets/mysecret2 && \
  TEST_ENV2=$(cat /run/secrets/mysecret2)

RUN echo ${TEST_ENV}
RUN echo ${TEST_ENV2}
