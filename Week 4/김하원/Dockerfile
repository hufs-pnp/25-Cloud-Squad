# FROM 베이스 이미지
ARG NODE_VERSION
FROM node:${NODE_VERSION}

# COPY <복사할 경로> <붙여넣기를 할 경로>
COPY . /app

# 소스코드 디렉토리
WORKDIR /app

# 소스코드 시작 (npm run)
RUN npm run 

# 환경변수 정의 
ENV PORT=27017

# 소스코드 실행
ENTRYPOINT ["start"]