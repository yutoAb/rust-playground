## ワークスペース構成

Cargo ワークスペースで複数クレートをまとめて管理している．
ルートの `Cargo.toml` に `[workspace]` を定義し，各クレートを members に登録する．

## 現在のクレート一覧

| クレート | 用途 | 外部依存 |
|---|---|---|
| `snippets/hello` | Hello World・基礎実験 | なし |
| `snippets/practice` | 自由な練習用 | なし |
| `katas/abc001` | AtCoder練習 | なし |
| `mini-projects/cli-todo` | CLIツール | `clap` |

## 基本コマンド

```bash
# 特定のクレートを実行
cargo run -p hello

# 全体ビルド
cargo build --workspace

# テスト
cargo test --workspace

# フォーマット
cargo fmt
```

## 新しい実験を追加する

```bash
cargo new snippets/テーマ名
# → ルートの Cargo.toml の members に自動追加される
cargo run -p テーマ名
```

## オフラインについて

- `cargo build` / `cargo run` / `cargo test` はオフラインで動く
- 外部クレートの新規追加（`cargo add`）はオンラインが必要
- ビルド済みのクレートはオフラインでも再ビルドできる

## Claude の resume

claude --resume 02ef9243-b50b-4729-9f87-4a51eb22707a