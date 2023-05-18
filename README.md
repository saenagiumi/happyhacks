# HappyHacks

<img src="./assets/main.png">

HappyHacksは、ADHDにありがちな困りごとの対策をシェアして、より良い環境調整を自分の生活に取り入れるためのサービスです。

### サービスURL
https://www.happyhacks.app/

## サービス紹介
--- 
### 工夫したところ
#### UX
- いいね、ブックマークのボタンをマイクロインタラクション
- プログレスバーを表示し、ロードが重いときに体感を軽くできるように
- 静的ページをSSGに、OGPが必要なところをSSRに
- レイアウトシフトをできるだけ無くせるように画像の高さ設定やスケルトンローディングなどを使用
- ブラウザバック時、スクロール位置の保存
- ブラウザバック時、前回まで開いていたタブの復元
- 画像ファイルをできるだけwebpなどにして圧縮
- 投稿の文字数が多いときは一覧にはすべて表示せず、「…もっと見る」で対応
- 詳細ページから投稿を見たままコメントやブックマークしたいときにリダイレクトせずログインできるように

#### スマホ対応
- レスポンシブ対応
- ボタン投稿ボタンをPCレイアウトとは変えた
- 文字が画面幅いっぱいまで詰まっていると目が疲れるんだなと思って右側80%くらいに寄せた
- 検索時、改行でなくキーボードに「検索」を表示しinputが表示されるように
- 検索ボタンを押したらキーボードが閉じるように、などUX面の考慮
- ボタンサイズなどが小さ過ぎて操作しづらくないかチェック

#### アクセシビリティ
- フォントと背景色のコントラスト比をチェックツールを使用して低くなり過ぎないように
- キーボードで遷移できないということがないかチェック
- alt属性の設定

## 使用した技術
---
### フロントエンド
- Next.js 13.2.4
- React 18.2.0
- TypeScript 4.9.4
- Tailwind CSS 3.2.4
- Mantine 5.9.4

#### 主要なライブラリ
- @auth0/auth0-react 2.0.0
- @next/font 13.2.4
- jotai 2.0.2
- next-seo 5.15.0
- swr 2.0.0
- axios 1.2.1
- dayjs 1.11.7
- @lottiefiles/react-lottie-player 3.5.2
- react-icons 4.7.1
- @vercel/og 0.5.0
- eslint 8.38.0
- prettier 2.8.7
- postcss 8.4.20

### バックエンド
- Rails 6.1.7 (APIモード)
- Ruby 3.1.3

#### 主要なgem
- rack-cors
- jwt
- annotate

### インフラ
- AWS (ECS / Fargate ECR ALB RDS(PostgreSQL) CloudWatch S3 Route53 Certificate Manager VPC)

### 外部サービス、その他
- Auth0
- Google Domains
- lottiefiles