# @jpc-yoshimatsu/nuxt3-dev-stack

Nuxt3環境でよく利用される基本的なパッケージスタックを管理するメタパッケージです。

## 概要

このパッケージは「メタパッケージ」（または「依存関係バンドル」）として機能し、実際のコードは含まず、依存関係の定義のみを提供します。これにより、全Nuxt3プロジェクトで一貫した依存関係のバージョン管理が可能になります。

## 特徴

### 🔄 自動更新対応
- Dependabotによる依存パッケージの自動更新監視
- 毎週月曜日午前8時（日本時間）に更新確認
- マイナーとパッチアップデートは1つのPull Requestにまとめて作成
- メジャーアップデートは個別のPull Requestとして作成
- セキュリティアップデートは検出次第、即時にPull Request作成

### 🎯 主なメリット

#### バージョン管理の一元化
- チーム/組織で使用する依存パッケージのバージョンを一箇所で管理
- 各プロジェクトでの個別バージョン指定が不要
- パッケージバージョンの整合性を保証

#### 一貫性の確保
- すべてのプロジェクトで同じバージョンの依存パッケージを使用
- 互換性の問題を事前に防止
- プロジェクト間の一貫性を維持

#### 更新の簡素化
- メタパッケージの更新だけで、依存プロジェクトの依存関係も更新
- Dependabotによる自動更新提案で、メンテナンスの手間を削減
- セキュリティアップデートの適用を効率化

## インストール

```bash
npm install @jpc-yoshimatsu/nuxt3-dev-stack
```

## 使用方法

このパッケージをインストールすると、定義されている全ての依存パッケージが自動的にプロジェクトにインストールされます。

### 必要な設定

プロジェクトの`.npmrc`ファイルに以下を追加してください：

```
@jpc-yoshimatsu:registry=https://npm.pkg.github.com
//npm.pkg.github.com/:_authToken=YOUR_GITHUB_TOKEN
```

`YOUR_GITHUB_TOKEN`は、GitHubの個人アクセストークンに置き換えてください。

## 含まれる依存パッケージ

現在、以下のパッケージが含まれています：

- `@iconify/vue` - アイコンコンポーネントライブラリ
- `@nuxt/eslint-config` - Nuxt3用のESLint設定
- `@nuxtjs/google-fonts` - Google Fontsの統合
- `@nuxtjs/seo` - SEO最適化モジュール
- `dayjs-nuxt` - 日付操作ライブラリ
- `eslint` - コード品質とスタイルチェック
- `nuxt` - Nuxt3フレームワーク本体
- `nuxt-gtag` - Google Analytics統合
- `sass` - Sassプリプロセッサ
- `vite-plugin-vuetify` - Vuetify用Viteプラグイン
- `vuetify` - マテリアルデザインコンポーネントフレームワーク

## バージョニング

このパッケージは[Semantic Versioning](https://semver.org/)に従います：
- MAJOR: 後方互換性のない変更
- MINOR: 後方互換性のある機能追加
- PATCH: 後方互換性のあるバグ修正

## ライセンス

MIT License 