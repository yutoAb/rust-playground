# 遊び方ガイド

## 1. まずはコードを書き換えて実行する

```bash
# snippets/hello/src/main.rs を好きなように書き換える
cargo run -p hello
```

これだけで動く．エラーが出たら，メッセージを読んで直す．

## 2. 所有権を体感してみる

`snippets/practice/src/main.rs` に以下を書いて実行:

```rust
fn main() {
    let s1 = String::from("hello");
    let s2 = s1;          // s1 の所有権が s2 に move
    println!("{}", s2);
    // println!("{}", s1); // ← コメントを外すとコンパイルエラー！
}
```

```bash
cargo run -p practice
```

コメントを外してエラーを確認し，なぜ動かないか考える．

## 3. 新しいテーマで実験する

```bash
cargo new snippets/好きな名前
# Cargo.toml の members に自動追加される
cargo run -p 好きな名前
```

例:
```bash
cargo new snippets/iterators
cargo run -p iterators
```

## 4. AtCoderの問題を解く

```bash
# katas/abc001/src/main.rs に解答を書く
echo "入力データ" | cargo run -p abc001
```

新しい問題用:
```bash
cargo new katas/abc002
cargo run -p abc002
```

## 5. CLIツールを作る

`mini-projects/cli-todo/src/main.rs` を編集する．
`clap` が使えるので，コマンドライン引数を受け取れる．

```bash
cargo run -p cli-todo
cargo run -p cli-todo -- --help
```

## よく使うコマンド一覧

| コマンド | 用途 |
|---|---|
| `cargo run -p クレート名` | 実行 |
| `cargo build --workspace` | 全体ビルド |
| `cargo test --workspace` | テスト実行 |
| `cargo fmt` | フォーマット |
| `cargo clippy` | 静的解析 |
| `cargo new snippets/名前` | 新しいクレート作成 |

## 困ったら

- コンパイルエラーのメッセージをよく読む（Rustのエラーは親切）
- `cargo check` でビルドせずに型チェックだけできる（速い）
- `memo.md` にクレート一覧とコマンドをまとめてある
