# Todo App (Go)

A simple and robust Todo application built with Go, featuring user authentication, multi-language support, and an MVC architecture.

Go言語で構築された、ユーザー認証、多言語対応、MVCアーキテクチャを備えたシンプルかつ堅牢なTodoアプリケーションです。

---

## English

### Features

- **User Authentication**: Secure signup, login, and logout functionality using UUIDs and encrypted passwords.
- **Todo Management**: Create, read, update, and delete your tasks.
- **Multi-language Support (i18n)**: Supports English and Japanese, determined by browser settings or user preference.
- **MVC Architecture**: Clean separation of concerns with Models, Views, and Controllers.
- **Database**: Uses SQLite3 for simple and portable data storage.
- **Docker Support**: Ready for containerized deployment with Docker and Docker Compose.
- **Configurable**: Easily adjust settings via `config.ini`.

### Tech Stack

- **Backend**: Go (Golang)
- **Database**: SQLite3
- **Frontend**: HTML Templates (standard library `html/template`)
- **Other**:
    - `google/uuid`: For unique session and user identifiers.
    - `go-sqlite3`: SQLite driver for Go.
    - `crypto`: Password hashing.
    - `ini.v1`: Configuration file management.

### Project Structure (Inside `src/todo_app`)

```
.
├── main.go            # Application entry point
├── config.ini         # Configuration file
├── app/               # Application logic
│   ├── controllers/   # Route handlers and server logic
│   ├── models/        # Database models and business logic
│   └── views/         # Templates, CSS, JS, and i18n data
├── config/            # Configuration loader
├── utils/             # Utility functions (logging, etc.)
└── Dockerfile         # Docker configuration
```

### Getting Started

#### Prerequisites

- Go 1.25 or higher
- Docker (optional)

#### Running Locally

1. **Navigate to the app directory**
   ```bash
   cd src/todo_app
   ```
2. **Install dependencies**
   ```bash
   go mod download
   ```
3. **Run the application**
   ```bash
   go run main.go
   ```
4. **Access the app**
   Open `http://localhost:8080` in your browser.

#### Running with Docker

1. **Navigate to the app directory**
   ```bash
   cd src/todo_app
   ```
2. **Start the containers**
   ```bash
   docker-compose up --build
   ```
3. **Access the app**
   Open `http://localhost:8080` in your browser.

---

## 日本語

### 特徴

- **ユーザー認証**: UUIDとパスワード暗号化を使用した安全なサインアップ、ログイン、ログアウト機能。
- **Todo管理**: タスクの作成、閲覧、更新、削除（CRUD機能）。
- **多言語対応 (i18n)**: 英語と日本語に対応。ブラウザ設定やユーザーの好みに応じて切り替わります。
- **MVCアーキテクチャ**: Model、View、Controllerによる明確な関心の分離。
- **データベース**: 軽量でポータブルなデータ保存のためにSQLite3を使用。
- **Docker対応**: DockerおよびDocker Composeによるコンテナ化されたデプロイが可能。
- **設定可能**: `config.ini`を通じて簡単に設定を調整できます。

### 使用技術

- **バックエンド**: Go (Golang)
- **データベース**: SQLite3
- **フロントエンド**: HTML テンプレート (標準ライブラリ `html/template`)
- **その他**:
    - `google/uuid`: ユニークなセッション・ユーザーID用。
    - `go-sqlite3`: Go用SQLiteドライバ。
    - `crypto`: パスワードのハッシュ化。
    - `ini.v1`: 設定ファイルの管理。

### プロジェクト構造 (`src/todo_app` 内)

```
.
├── main.go            # アプリケーションのエントリーポイント
├── config.ini         # 設定ファイル
├── app/               # アプリケーションロジック
│   ├── controllers/   # ルートハンドラとサーバーロジック
│   ├── models/        # データベースモデルとビジネスロジック
│   └── views/         # テンプレート、CSS、JS、多言語データ
├── config/            # 設定ローダー
├── utils/             # ユーティリティ関数（ロギングなど）
└── Dockerfile         # Docker設定
```

### はじめかた

#### 必須条件

- Go 1.25 以上
- Docker (オプション)

#### ローカルでの実行

1. **アプリディレクトリに移動**
   ```bash
   cd src/todo_app
   ```
2. **依存関係をインストールする**
   ```bash
   go mod download
   ```
3. **アプリケーションを実行する**
   ```bash
   go run main.go
   ```
4. **アプリにアクセスする**
   ブラウザで `http://localhost:8080` を開きます。

#### Docker での実行

1. **アプリディレクトリに移動**
   ```bash
   cd src/todo_app
   ```
2. **コンテナを起動する**
   ```bash
   docker-compose up --build
   ```
3. **アプリにアクセスする**
   ブラウザで `http://localhost:8080` を開きます。
