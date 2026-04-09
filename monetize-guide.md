# ぼやきログ 収益化セットアップガイド

## ① Google AdSense（アドセンス）の登録手順

### 必要なもの
- Googleアカウント
- ブログのURL（自分のドメインが必要：例 `boyakilog.com`）
- 記事がある程度揃っていること（最低10〜15記事が目安）

### 登録手順

1. https://adsense.google.com にアクセス
2. 「ご利用開始」をクリックしてGoogleアカウントでログイン
3. サイトのURLを入力して申請
4. 審査用のコードを `<head>` タグ内に貼り付ける
5. 審査を待つ（数日〜数週間かかることもある）
6. 審査通過後、パブリッシャーID（`ca-pub-XXXX`）が発行される

### HTMLへの貼り方

`nioh3-guide.html` の中にコメントで場所を示してあります。

```html
<!-- HEAD内に貼る（サイト全体に適用） -->
<script async
  src="https://pagead2.googlesyndication.com/pagead/js/adsbygoogle.js?client=ca-pub-あなたのID"
  crossorigin="anonymous">
</script>

<!-- 広告を表示したい場所に貼る -->
<ins class="adsbygoogle"
  style="display:block"
  data-ad-client="ca-pub-あなたのID"
  data-ad-slot="あなたのスロットID"
  data-ad-format="auto"
  data-full-width-responsive="true">
</ins>
<script>(adsbygoogle = window.adsbygoogle || []).push({});</script>
```

---

## ② Amazonアソシエイト（アフィリエイト）の登録手順

### 必要なもの
- Amazonのアカウント
- ブログのURL

### 登録手順

1. https://affiliate.amazon.co.jp にアクセス
2. 「今すぐ登録」からAmazonアカウントでログイン
3. ウェブサイトURLや紹介内容を入力（ゲームブログと書けばOK）
4. 登録完了後、商品リンクが作れるようになる

### リンクの作り方

Amazonで商品を検索 → 商品ページで「テキストを取得」→ URLをコピー

```html
<!-- nioh3-guide.html の aff-btn の href に貼り付ける -->
<a href="https://www.amazon.co.jp/dp/商品ID/?tag=あなたのタグID"
   class="aff-btn btn-amazon" target="_blank" rel="noopener">
  Amazonで見る
</a>
```

---

## ③ 楽天アフィリエイトの登録手順

1. https://affiliate.rakuten.co.jp にアクセス
2. 楽天IDで登録
3. 商品リンクを発行してコピー → `btn-rakuten` の href に貼り付ける

---

## ④ 記事を書く際のSEOポイント（検索から読者を呼ぶコツ）

- タイトルに「【仁王3】」「攻略」「初心者」などのキーワードを入れる
- 記事の最初に「この記事でわかること」をまとめる
- 見出し（h2, h3）にキーワードを含める
- 最後に「関連記事」を設置して回遊を促す

---

## ⑤ ブログを公開するには

HTMLファイルをローカルで開くだけではネット上に公開されません。
以下のいずれかで公開できます。

### 無料でできる方法（おすすめ）

| サービス | 特徴 |
|----------|------|
| GitHub Pages | 無料・独自ドメイン対応・HTML直接アップロードOK |
| Netlify | 無料・最も簡単・ドラッグ＆ドロップで公開 |
| Xserver | 有料（月数百円）だが国内で安定・AdSense審査も通りやすい |

### 最も簡単な方法：Netlify

1. https://netlify.com にアクセス・アカウント作成
2. 「Add new site」→「Deploy manually」
3. HTMLファイル（またはフォルダ）をドラッグ＆ドロップ
4. 数秒で公開完了（`xxxx.netlify.app` というURLが発行される）
5. 独自ドメイン（`boyakilog.com` など）を取得して紐付けるとより本格的

---

## まとめ：収益化への大まかな流れ

```
1. ブログを公開（Netlify等）
      ↓
2. 記事を10〜15本書く
      ↓
3. Google AdSense に申請
      ↓
4. Amazonアソシエイト・楽天アフィリエイトに登録
      ↓
5. 記事にコードを貼り付けて完成！
      ↓
6. 記事を増やしてアクセスを伸ばす
```

焦らず、まずは「記事を書き続けること」が一番大事です！
```
