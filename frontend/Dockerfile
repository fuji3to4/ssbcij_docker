# Node.jsベースイメージ
FROM node:20

# 作業ディレクトリを作成
WORKDIR /app

# package.json と package-lock.json を先にコピー
COPY ./word-haku/package*.json /app/

# 依存関係をインストール
RUN npm install

# アプリコードをコピー
COPY ./word-haku /app

# Next.jsビルド
RUN npm run build


# サーバー起動コマンド
CMD ["npm", "start"]
