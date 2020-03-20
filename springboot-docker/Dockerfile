#openjdk8
FROM openjdk:8

MAINTAINER zero <zhangszi0291@gmail.com>

#设置工作路径和jar包名字
ARG workpath=/opt/rework/
ARG jarname=rework.jar
WORKDIR ${workpath}
ENV JAR=${workpath}/${jarname}

#添加springboot的jar文件到指定目录并重命名
ADD rework-0.1-SNAPSHOT.jar ${workpath}/${jarname}

#添加spring配置参数
ARG SPRING_OPTS
ENV SPRING_OPTS=${SPRING_OPTS}
#添加JVM配置参数
ARG JAVA_OPTS
ENV JAVA_OPTS=${SPRING_OPTS}

ENTRYPOINT java ${JAVA_OPTS} -Djava.security.egd=file:/dev/./urandom -jar ${JAR}  ${SPRING_OPTS}

#启动
#docker create --name rework --network=host  -v /home/zero/logs:/opt/rework/logs -e JAVA_OPTS="$JAVA_OPTS" -e SPRING_OPTS="$SPRING_OPTS" rework