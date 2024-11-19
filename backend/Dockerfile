# Pythonベースイメージ
FROM python:3.12-slim

# 作業ディレクトリを作成
WORKDIR /app

# Poetryをインストール
RUN pip install --no-cache-dir poetry

# Poetry設定: 仮想環境を無効化
RUN poetry config virtualenvs.create false

COPY ./word_haku_api /app
#COPY .env /app/word_haku_api/.env

# 依存関係をインストール
RUN poetry install


# FastAPIの起動コマンド
CMD ["bash", "-c", "cd /app/word_haku_api && poetry run uvicorn main:app --host 0.0.0.0 --reload"]

