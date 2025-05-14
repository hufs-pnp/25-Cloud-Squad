# FROM 베이스 이미지
ARG NODE_VERSION=20.15.1
FROM node:${NODE_VERSION}

# COPY <복사할 경로> <붙여넣기를 할 경로>
COPY . /apps/mbti

# 소스코드 디렉토리
WORKDIR /apps/mbti

# 소스코드 시작 (npm run)
RUN npm install

# 환경변수 정의 
ENV PORT=3001 \
    DB_HOST=localhost \
    DB_PORT=3306 \
    DB_NAME=db_mbti \
    DB_USERNAME=user_mbti \
    DB_PASSWORD=pw_mbti

EXPOSE 3001

# 소스코드 실행
ENTRYPOINT ["npm", "start"]