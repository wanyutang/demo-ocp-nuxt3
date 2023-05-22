# 使用 Node 14 作為基礎映像
FROM node:14

# 設置工作目錄
WORKDIR /app

# 複製專案文件到容器中
COPY . .

# 安裝相依套件
RUN npm install

# 設定使用者和群組為 node
RUN chown -R node:node /app

# 切換使用者為 node
USER node

# 建構專案
#RUN npm run build

# 發佈網站
#CMD ["npx", "nuxt", "start"]

# 開放Nuxt應用程式的預設埠
EXPOSE 3000

# 定義執行時指令
CMD ["npm", "run", "dev"]
