# slo homes — Vercel デプロイ手順

静的サイトです。ビルド設定は不要です。写真はすべて圧縮済みで、全体で約 4MB です。

## 含まれるファイル

- `index.html` — 公開用トップページ（JA / EN 切替つき）
- `support.js` — ページの実行に必要
- `_ds/` — フォントとデザイントークン
- `assets/` — 写真・周辺図・図面PDF
- `japan-map.html` — Location の日本地図
- `slo-homes.dc.html` — 編集用のコピー（公開には不要）

## 手順

1. GitHub で新しいリポジトリを作成（Private でも可）
2. zip を展開し、中身をそのまま push

```bash
git init
git add .
git commit -m "slo homes site"
git branch -M main
git remote add origin https://github.com/<user>/<repo>.git
git push -u origin main
```

3. [vercel.com/new](https://vercel.com/new) でそのリポジトリを Import
4. Framework Preset は **Other**、Build Command と Output Directory は空のまま Deploy

`index.html` がルートにあるので、そのまま公開されます。

## 補足

- 独自ドメインは Vercel の Project → Settings → Domains から設定できます
- 写真を差し替える場合は `assets/` のファイルを同名で置き換えて push すれば反映されます
- 非公開にしたい場合は Vercel の Deployment Protection（Password / Vercel Authentication）を有効にしてください
- GitHub は1ファイル100MB・推奨リポジトリ50MB以下が目安です。今の構成はその範囲内です
