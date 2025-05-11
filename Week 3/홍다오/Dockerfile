# 1. 베이스 이미지 설정
ARG NODE_VERSION=20.15.1
FROM node:${NODE_VERSION}

# 2. 작업 디렉토리 설정
WORKDIR /apps/mbti

# 3. node_modules 제외한 복사 (사전에 .dockerignore 필요)
COPY package*.json ./
RUN npm install

# 4. 전체 소스 복사
COPY . .

# 5. 환경 변수 정의
ENV PORT=3001 \
    DB_HOST=localhost \
    DB_PORT=3306 \
    DB_NAME=db_mbti \
    DB_USERNAME=user_mbti \
    DB_PASSWORD=pw_mbti

# 6. 포트 노출
EXPOSE 3001

# 7. 실행 명령 설정
CMD ["npm", "start"]