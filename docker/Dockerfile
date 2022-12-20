FROM nginx:latest

RUN env

# このマウントの仕方はOK. 多分ここで参照しないと揮発する。
RUN --mount=type=secret,id=mysecret,uid=0 cat /run/secrets/mysecret \
  echo `ls -a /` \
  echo `ls -a /run/` \
  echo `ls -a /run/secrets/`
RUN --mount=type=secret,id=mysecret2,uid=0 cat /run/secrets/mysecret2 \
  echo `ls -a /` \
  echo `ls -a /run/` \
  echo `ls -a /run/secrets/`

RUN echo `ls -a /`
RUN echo `ls -a /run/`
RUN echo `ls -a /run/secrets/`
RUN TEST_ENV=$(cat /run/secrets/mysecret)
RUN echo ${TEST_ENV}
