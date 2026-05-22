# CareerLink Bonus — フィッシング詐欺 注意喚起デモ

就活生を狙ったフィッシング詐欺の手口を**体験形式**で学べる、静的HTMLの啓発デモサイトです。  
周囲でSNSアカウントの乗っ取り被害が相次いでいることを受け、同じ手口に引っかからないよう友人へのシェアを目的として作成しました。

---

## デモの流れ

```
① 偽サイト画面
  └─ 就活紹介キャンペーンを装ったランディングページ
  └─ 「LINEで続ける」ボタンを押す

② ローディング画面
  └─ 「LINE認証に接続中…」のスピナー（約2秒）
  └─ 自動で③へ遷移

③ タネ明かし画面
  └─ 「これは偽サイトの再現デモです」と告知
  └─ 詐欺の手口・危険サインの解説
  └─ URLの本物／偽物チェック練習
  └─ 今すぐできる対策
  └─ 公式資料へのリンク
```

---

## 収集している情報

**個人情報・LINE情報・認証コードは一切取得していません。**  
すべてのロジックはクライアントサイドのJavaScript（画面切り替えのみ）で完結しており、外部へのデータ送信は行いません。

---

## ファイル構成

```
index.html   # すべて1ファイルで完結（HTML / CSS / JS）
README.md    # このファイル
```

外部依存はGoogle Fonts（Noto Sans JP / DM Mono）のみです。フォント読み込みが不要な環境ではhead内の`<link>`を削除してください。

---

## デプロイ方法

`index.html` を任意のホスティングサービスに置くだけで動作します。

**GitHub Pages を使う場合**

```bash
git init
git add .
git commit -m "init"
git remote add origin https://github.com/<user>/<repo>.git
git push -u origin main
# Settings → Pages → Branch: main / root で公開
```

公開後、`index.html` 内の OGP URL を実際のURLに変更してください。

```html
<meta property="og:url" content="https://<your-domain>/" />
```

---

## 掲載している公式資料

| 機関 | リンク |
|---|---|
| 国民生活センター | https://www.kokusen.go.jp/pdf/n-20221221_2.pdf |
| フィッシング対策協議会 | https://www.antiphishing.jp/ |
| 警察庁 サイバー局 | https://www.npa.go.jp/bureau/cyber/countermeasures/phishing.html |
| LINE 公式（乗っ取り被害に遭ったら） | https://support.line.me/hc/ja/articles/115003505631 |

---

## ライセンス・商標について

- LINEの名称・ロゴ・カラーは **LINE ヤフー株式会社** の商標です。本デモはLINE社とは無関係であり、公式サービスを模倣・代替するものではありません。
- 本デモを改変・再配布する場合も、情報収集を行わないこと・啓発目的に限ること・商標に関する表記を維持することを守ってください。
