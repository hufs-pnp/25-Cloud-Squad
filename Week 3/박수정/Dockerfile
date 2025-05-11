# FROM 베이스 이미지
FROM node:20.15.1

# 소스코드 디렉토리
WORKDIR /apps/mbti

# COPY <복사할 경로> <붙여넣기를 할 경로>
COPY package*.json ./
RUN npm install

COPY . .

# 환경변수 정의 
ENV PORT=3301 \
    DB_HOST=localhost \
    DB_PORT=3306 \
    DB_NAME=db_mbti \
    DB_USERNAME=user_mbti \
    DB_PASSWORD=pw_mbti

# 소스코드 실행
CMD ["npm", "run", "start"]
