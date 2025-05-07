# 1. 베이스 이미지
FROM node:20.15.1

# 2. 작업 디렉토리 설정
WORKDIR /apps/mbti

# 3. 패키지 복사 (node_modules 제외)
COPY package*.json ./
RUN npm install

# 4. 애플리케이션 소스 복사
COPY . .

# 5. 환경 변수 설정 
ENV PORT=3001 \
    DB_HOST=localhost \
    DB_PORT=3306 \
    DB_NAME=db_mbti \
    DB_USERNAME=user_mbti \
    DB_PASSWORD=pw_mbti

# 6. 앱 실행 포트 개방
EXPOSE 3001

# 7. 앱 실행 명령
CMD ["npm", "run", "start"]
