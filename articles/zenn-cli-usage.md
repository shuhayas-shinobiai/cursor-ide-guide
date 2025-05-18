---
title: "Zenn CLIの使い方"
emoji: "📝"
type: "tech" # tech: 技術記事 / idea: アイデア
topics: ["zenn", "markdown", "cli"]
published: false
---

# Zenn CLIの使い方

Zenn CLIを使うと、ローカル環境で記事を作成し、プレビューすることができます。この記事では、Zenn CLIのインストール方法から使い方まで詳しく解説します。

## インストール方法

Zenn CLIをインストールするには、以下のコマンドを実行します：

```bash
npm install zenn-cli
```

## 初期設定

インストール後、以下のコマンドで初期設定を行います：

```bash
npx zenn init
```

これにより、必要なディレクトリやファイルが作成されます。

## 記事の作成

新しい記事を作成するには、以下のコマンドを実行します：

```bash
npx zenn new:article
```

これにより、`articles/`ディレクトリに新しいマークダウンファイルが作成されます。

記事のファイル名は自動的に生成されますが、以下のようにオプションを指定することもできます：

```bash
npx zenn new:article --slug zenn-cli-usage --title "Zenn CLIの使い方" --type tech --emoji 📝
```

## プレビュー

作成した記事をプレビューするには、以下のコマンドを実行します：

```bash
npx zenn preview
```

ブラウザで`http://localhost:8000`にアクセスすると、記事のプレビューが表示されます。

## 記事の公開

記事を公開するには、GitHubリポジトリにプッシュします：

```bash
git add .
git commit -m "記事を追加"
git push
```

その後、Zennのウェブサイトで公開設定を行います。記事のフロントマターにある`published: false`を`published: true`に変更することで、記事が公開されます。

## GitHub連携のメリット

Zennは、GitHubリポジトリと連携することで、より効率的に記事を管理することができます：

1. **バージョン管理**: GitHubを使用して記事の変更履歴を管理できます
2. **コラボレーション**: 複数人での記事作成・レビューが可能になります
3. **CI/CD**: GitHub Actionsなどを使用して、記事の自動チェックや公開が可能になります
4. **バックアップ**: 記事のバックアップとしても機能します

## まとめ

Zenn CLIを使うことで、ローカル環境で快適に記事を作成し、プレビューすることができます。また、GitHubと連携することで、効率的に記事を管理・公開することができます。

Zenn CLIの詳細については、[公式ドキュメント](https://zenn.dev/zenn/articles/zenn-cli-guide)を参照してください。
