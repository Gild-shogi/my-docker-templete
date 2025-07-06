## Jupyter環境
- JupyterLabの立ち上げ環境

### パッケージ管理：uv
- 依存関係の管理：`uv sync`
- パッケージの追加：`uv add <package_name>`
- パッケージの削除：`uv remove <package_name>`
- requirements.txtへのexport：`uv export --format requirements-txt > requirements.txt`

### 開発環境セットアップ
1. 依存関係のインストール：`uv sync`
2. JupyterLabの起動：`docker compose up --build -d`
3. 停止：`docker compose down`

### コード品質管理
- Lint実行：`uv run ruff check`
- Lintの自動修正：`uv run ruff check --fix`
- フォーマット：`uv run ruff format`

### 注意事項
- 新しいパッケージを追加した場合は、必ず`uv sync`を実行してください
- コードのコミット前には必ずlintチェックを実行してください
