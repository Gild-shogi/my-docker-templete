# FastAPI アプリケーション

FastAPIアプリケーションのテンプレートです。

## 環境構築

### 1. 依存関係のインストール

```bash
uv sync
```

### 2. アプリケーションの起動

#### Dockerを使用した起動（推奨）

```bash
docker compose up -d
```

アプリケーションは http://localhost:8000 でアクセス可能です。

#### 開発環境での起動

```bash
uv run uvicorn app.main:app --reload
```

### コード品質管理
- Lint実行：`uv run ruff check`
- Lintの自動修正：`uv run ruff check --fix`
- フォーマット：`uv run ruff format`


## 構成

- **パッケージ管理**: uv
- **アプリケーション起動**: Docker Compose
- **データベース**: PostgreSQL 16
- **アプリケーション**: FastAPI + Uvicorn
