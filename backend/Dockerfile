FROM python:3.11-slim

WORKDIR /app

# 依存ライブラリをインストール
COPY ./app/requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt

# アプリ本体をコピー
COPY ./app ./app

# uvicorn で起動
CMD ["uvicorn", "app.main:app", "--host", "0.0.0.0", "--port", "8000", "--reload"]
