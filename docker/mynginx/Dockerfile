#获取Linux基础镜像
FROM registry.saas.hand-china.com/tools/alpine:3.7-1

MAINTAINER jingjinzhang

ENV HUGO_SITE=hugo_blog

COPY hugo_blog/ /hugo_blog/
ADD /hugo_0.44_Linux-64bit.tar.gz /tmp
RUN mv /tmp/hugo /usr/local/bin/

WORKDIR ${HUGO_SITE}

EXPOSE 1313

ENV HUGO_BASE_URL http://localhost:1313
CMD hugo server -b ${HUGO_BASE_URL} --bind=0.0.0.0

