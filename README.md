# 数式の「変身」のひみつ

～プログラミングの「評価」を学ぼう～

[Slidev](https://github.com/slidevjs/slidev) で作った小学生向け教材スライドです。「式」が「値」へ評価される過程を、[Shiki Magic Move](https://sli.dev/features/shiki-magic-move) でコードが少しずつ書き換わるアニメーションとして可視化しています。

## スライドを見る

```bash
pnpm install
pnpm run dev
```

起動後 <http://localhost:3030> にアクセスしてください。

内容を編集する場合は [slides.md](./slides.md) を、共通のフォント・コードのスタイルは [style.css](./style.css) を変更してください。

## ビルド

```bash
pnpm run build
```

`dist/` に静的サイトが出力されます。

## デプロイ

`main` ブランチに push すると [GitHub Actions](.github/workflows/deploy-pages.yml) が自動でビルドし、GitHub Pages に公開します(リポジトリの Settings → Pages → Source を「GitHub Actions」にしておく必要があります)。

公開URL: <https://osad-sakana.github.io/evaluation/>

## 使用技術

- [Slidev](https://sli.dev/)
- [Shiki Magic Move](https://sli.dev/features/shiki-magic-move) — コードの変化をステップごとにアニメーション表示
- フォント: [BIZ UDゴシック](https://fonts.google.com/specimen/BIZ+UDGothic)(本文) / [0xProto](https://fonts.google.com/specimen/0xProto)(コード)
