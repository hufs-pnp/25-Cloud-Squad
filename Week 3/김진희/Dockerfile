FROM node:20.15.1

WORKDIR /apps/mbti

COPY . .

RUN npm install

ENV PORT=3001 \
    DB_HOST=localhost \
    DB_PORT=3306 \
    DB_NAME=db_mbti \
    DB_USERNAME=user_mbti \
    DB_PASSWORD=pw_mbti

CMD ["npm", "start"]