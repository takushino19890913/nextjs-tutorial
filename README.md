# Link Componentを使うことによってClient-side navigationを使うことができる。
- クライアントの状態を保ってページ遷移。
  →例えば検索結果を表示する際にページが切り替わってもクエリー等を指定しなくても実行可能。
- そして早い。
- Next.jsではルーティングの設定が不要。pagesディレクトリ内での相対パスがそのままURLとなる。

```js
import Link from "next/link";

export default function Hoge () => {
  return (
    <Link href="/hoge/fuga">
      <a>Go to fuga</a>
    </Link>
  )
}
```

# Public Directory
- imageなど静的ファイルを置く場所。
- SEO対策のrobots.txtも置ける。

# CSS Modules
 個別のページに読み込むCSS
### 手順
- layout.jsを作る。
- layout.modules.cssを作る。
- layout.js内で定義したLayoutコンポーネントで装飾したいページのjsxをラップする。

# _app.js
- 特殊なファイルで、Routeコンポーネントをラップする。
- グローバルCSSやその他グローバル処理を実行。
