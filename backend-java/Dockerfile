# 베이스 이미지 설정
FROM openjdk:17-jdk-slim

# 작업 디렉토리 설정
WORKDIR /app
# JAR 파일 경로를 ARG로 받아서 복사
ARG JAR_PATH
COPY ${JAR_PATH} app.jar

# 컨테이너 실행 시 실행할 명령어 설정
ENTRYPOINT ["java", "-jar", "app.jar"]