# Node 설치. (이미지 관점 - 맨 아래 Layer (Base image))
# FROM 베이스 이미지
ARG NODE_VERSION
FROM node:${NODE_VERSION}

# 소스코드 다운로드
# COPY <복사할 경로> <붙여넣기를 할 경로>
COPY . /apps/mbti

# 소스코드의 최상단 디렉토리로 이동
WORKDIR /apps/mbti

# 소스코드를 실행할 때 필요한 파일 다운로드 (npm ci)
# 소스코드를 빌드 (npm run build)
RUN npm ci \
&& npm run build

# 환경변수 정의 (PORT)
ENV PORT="3000" \
    DB_HOST="localhost" \
    DB_PORT="3306" \
    DB_NAME="db_mbti" \
    DB_USERNAME="user_mbti" \
    DB_PASSWORD="pw_mbti"

# 소스코드 실행 (npm run start)
ENTRYPOINT ["npm", "run", "start"]
