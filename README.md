# IM\@S Gallery

**アイドルマスターシリーズの画像を投稿・共有するためのギャラリーサービス**

IM\@S Galleryは、アイドルマスターシリーズに登場するアイドルの画像を投稿・閲覧・共有できるWebサービスです。

ブランド・アイドル・タグによる分類や、投稿前の審査機能などを備え、シリーズ全体のファンが利用できるギャラリーを目指して開発しています。

## About

本プロジェクトは、Kikuflare氏が開発した **imas765probot** を起点として構想・開発を進めているものです。

当初の構想から発展し、765PRO ALLSTARSに限定しない、アイドルマスターシリーズ全体を対象とした独立したWebサービスとして再構築しています。

IM\@S Galleryは、特定のSNSや外部サービスに依存せず、独立して利用できるサービスを目指しています。

## Features

実装予定・開発中の主な機能です。

- **Image Gallery** — 投稿された画像の閲覧・検索
- **Idol List** — ブランド別・アイドル別の一覧
- **Tag System** — タグによる画像の分類・検索
- **Image Upload** — ユーザーによる画像投稿
- **Post Moderation** — 公開前の投稿審査
- **User Accounts** — ユーザー登録・ログイン・プロフィール
- **X Account Integration** — Xアカウントとの任意連携
- **Official X Posting** — 条件を満たした投稿の公式Xアカウントへの自動投稿（将来実装予定）

※機能は開発状況に応じて変更される場合があります。

## Technology Stack

| Category         | Technology        |
| ---------------- | ----------------- |
| OS               | Debian GNU/Linux  |
| Web Server       | Apache            |
| Backend          | Node.js / Express |
| Frontend         | React             |
| Database         | MariaDB           |
| Query Builder    | Knex.js           |
| Image Processing | Sharp             |
| Version Control  | Git / GitHub      |

## Architecture

基本的な構成は以下を予定しています。

```text
Client
  |
  | HTTPS
  v
Apache
  |
  +---- React Frontend
  |
  +---- Node.js / Express
             |
             +---- MariaDB
             |
             +---- Image Storage
             |
             +---- External Services
```

画像ファイル本体はデータベースに格納せず、ファイルシステム上で管理します。

投稿された画像は審査前の隔離領域に保存し、承認後に公開領域へ移動する設計を予定しています。

## Development

現在は開発初期段階です。

開発環境・デプロイ環境にはRaspberry Piを使用し、Linux上での運用を想定しています。

今後、開発状況に応じてCI/CDや自動テストなども導入する予定です。

## Project Status

**Under Development**

現在は基本設計および開発環境の構築を進めています。

認証・投稿・審査・画像管理など、サービスの基盤となる機能から順次実装していく予定です。

## Disclaimer

IM\@S Galleryは、アイドルマスターシリーズのファンによる非公式のプロジェクトです。

株式会社バンダイナムコエンターテインメントおよび関連企業とは関係ありません。

本プロジェクトは、アイドルマスターシリーズの公式サービスではありません。

本サービスに投稿される画像の著作権・利用許諾については、投稿者および各権利者の権利を尊重します。

## License

License: To be determined.

ライセンスについては、今後の開発方針に応じて決定します。
