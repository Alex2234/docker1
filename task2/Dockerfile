FROM node:16-alpine

# Задать рабочую директорию
WORKDIR /home/ilovedocker/app

COPY package*.json ./
# Флаг --omit=dev означает - "не ставить devDependencies"
# они не нужны нам в продакшен-окружении
RUN npm i --omit=dev
# копируем исходный код
COPY . .

EXPOSE 3000
CMD [ "node", "index.js" ] 
# Задать скрипт в качестве команды запуска
CMD ["sh", "hello.sh"]
