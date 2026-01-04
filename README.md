# GitHub CI/CD 実践ガイド

書籍「**GitHub CI/CD 実践ガイド**」を読みながら、ハンズオン形式で GitHub Actions を学習するためのリポジトリ集です。

## 📚 概要

このリポジトリは、書籍「GitHub CI/CD 実践ガイド」の各章・セクションに対応したハンズオン用リポジトリを管理する親リポジトリです。

各章の学習内容を個別のリポジトリとして作成し、実際に手を動かしながら GitHub Actions の使い方を習得します。

## 🗂️ 各章のリポジトリ

各リポジトリ名に使用している数字は、書籍「GitHub CI/CD 実践ガイド」のセクション番号に連動しています。

### 第6章

- [gcpg-6-2](https://github.com/striderkein/gcpg-6-2) - 第6章セクション2

<!-- 新しい章のリポジトリを追加する際は、上記の形式で追記してください -->

## 📝 リポジトリ命名規則

子リポジトリは以下の命名規則に従います：

```
gcpg-{章番号}-{セクション番号}
```

例：
- `gcpg-6-2` → 第6章セクション2
- `gcpg-1-1` → 第1章セクション1

## 🔍 検索方法

GitHub の Topics 機能を活用して、関連するリポジトリを検索できます：

- `github-cicd-practice-guide` - この書籍の学習リポジトリ
- `handson` - ハンズオン形式のリポジトリ
- `cicd` - CI/CD 関連
- `github-actions` - GitHub Actions 関連

## 🤖 自動化機能

このリポジトリには、新しい章・セクションのハンズオン用リポジトリを自動的に作成する機能があります。

### テンプレートリポジトリ

新しいリポジトリは、テンプレートリポジトリ `github-cicd-practice-guide-handson` から作成されます。

### 新しいリポジトリの作成方法

1. [イシューテンプレート「START_NEW_SECTION」](https://github.com/striderkein/github-cicd-practice-guide/issues/new?template=START_NEW_SECTION.md) を使用してイシューを作成
2. イシューのタイトルを `gcpg-{章番号}-{セクション番号}` の形式で設定（例: `gcpg-1-1`）
3. GitHub Actions が自動的に以下を実行します：
   - テンプレートリポジトリ `github-cicd-practice-guide-handson` から新しい public リポジトリを作成
   - 命名規則に従ったリポジトリ名を設定
   - トピックスを自動付与（`github-cicd-practice-guide`, `handson`, `cicd`, `github-actions`）
   - READMEのプレースホルダー（`{CHAPTER}`, `{SECTION}`）を実際の値に置換

### 注意事項

- **Personal Access Token (PAT) の設定が必要な場合があります**
  - `GITHUB_TOKEN` では他のリポジトリを作成できない場合があります
  - その場合は、以下の手順でPATを設定してください：
    1. [GitHub Settings > Developer settings > Personal access tokens](https://github.com/settings/tokens) でPATを作成
    2. 必要な権限: `repo` (すべてのリポジトリへのフルアクセス)
    3. このリポジトリの Settings > Secrets and variables > Actions で `REPO_CREATION_TOKEN` という名前でPATを設定

## 📖 使い方

1. 各章のリポジトリを個別にクローンして学習を進めます
2. 各リポジトリの README に記載されている手順に従ってハンズオンを実施します
3. 学習内容は各リポジトリにコミット・プッシュして記録します

## 🔗 関連リンク

- [書籍: GitHub CI/CD 実践ガイド](https://gihyo.jp/book/2024/978-4-297-14173-8)

---

> 💡 **Tip**: 各子リポジトリの README には、この親リポジトリへのリンクが記載されています。
