FROM nginx:latest

RUN env

# 1. docker build 時に `id` を明示的に指定する場合（例: `--secret id=my_env1,env=MY_ENV1` ）
RUN --mount=type=secret,id=mysecret cat /run/secrets/mysecret \
  TEST_ENV=$(cat /run/secrets/mysecret)

RUN echo ${TEST_ENV}
