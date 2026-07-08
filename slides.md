---
theme: seriph
background: https://cover.sli.dev
title: 数式の「変身」のひみつ
info: |
  ## 数式の「変身」のひみつ
  ～プログラミングの「評価」を学ぼう～

  小学生向け教材スライド
class: text-center
drawings:
  persist: false
transition: slide-left
mdc: true
duration: 20min
fonts:
  sans: 'BIZ UDGothic'
  serif: 'BIZ UDGothic'
  mono: '0xProto'
---

# 数式の「変身」のひみつ

～プログラミングの「評価」を学ぼう～

<div class="mt-12 py-1">
  Press Space for next page <carbon:arrow-right class="inline"/>
</div>

---
transition: fade-out
---

# 1. まずは算数の話から

`3 + 5` を見たら、頭の中で自然に `8` に計算するはず。

<div class="grid grid-cols-2 gap-8 items-center mt-6">
<div>

<v-clicks>

- このとき、`3 + 5` という「まだ計算していないもの」が、`8` という「答え」に変わっている。
- プログラミングの世界では、この「答えに変わること」を<strong>評価（ひょうか）</strong>と呼ぶ。
- むずかしい言葉に見えるけど、やっていることは今の計算と同じ。

</v-clicks>

</div>
<div class="flex flex-col items-center gap-3 big-eval-code">

````md magic-move
```js
3 + 5
```

```js
8
```
````

<div v-click class="text-sm opacity-70 mt-2">式 → 評価 → 値</div>

</div>
</div>

---

# 2. 「式」と「値」はちがうもの

プログラムの中には2つの状態がある。

| よび方 | 例 | どんなもの？ |
| --- | --- | --- |
| 式（しき） | `3 + 5` | まだ計算する前 |
| 値（あたい） | `8` | 計算し終わった後 |

<v-click>

<div class="flex items-center justify-center gap-6 mt-10">
  <div class="px-8 py-5 rounded-lg border-2 border-blue-400 bg-blue-400/10 text-center">
    <div class="text-sm opacity-70">式</div>
    <div class="text-2xl font-bold font-mono mt-1">3 + 5</div>
  </div>
  <div class="text-3xl text-orange-500">
    <carbon:arrow-right />
  </div>
  <div class="px-8 py-5 rounded-lg border-2 border-orange-400 bg-orange-400/10 text-center">
    <div class="text-sm opacity-70">値</div>
    <div class="text-2xl font-bold font-mono mt-1">8</div>
  </div>
</div>
<div class="text-center text-sm opacity-60 mt-3">評価されると、式は値にすがたを変える</div>

</v-click>

<v-click>

<div class="mt-6 text-center">
コンピュータは式のままでは使えなくて、必ず値にしてからでないと次に進めない。
</div>

</v-click>

---

# 3. 関数は「自動販売機」に似ている

自動販売機にお金を入れてボタンを押すと、ジュースが出てくる。

`add` のような関数（機械）も、まったく同じ仕組みで動いている。

<div class="flex items-center justify-center gap-4 mt-10">
  <div class="flex flex-col gap-2">
    <div class="px-4 py-2 rounded-lg border-2 border-blue-400 bg-blue-400/10 text-center font-mono">3</div>
    <div class="px-4 py-2 rounded-lg border-2 border-blue-400 bg-blue-400/10 text-center font-mono">5</div>
  </div>
  <div class="text-2xl opacity-60"><carbon:arrow-right /></div>
  <div class="px-6 py-8 rounded-lg border-2 border-primary bg-primary/10 text-center">
    <div class="text-3xl">🥤</div>
    <div class="font-mono mt-1">add</div>
  </div>
  <div class="text-2xl opacity-60"><carbon:arrow-right /></div>
  <div class="px-6 py-6 rounded-lg border-2 border-orange-400 bg-orange-400/10 text-center font-mono text-2xl font-bold">8</div>
</div>

<div class="mt-8">

<v-clicks>

- 材料（引数）を入れてボタンを押すと → 「式」（まだ何も出ていない状態）
- ジュース（戻り値）が出てくる → 「値」（結果が出た状態）
- 「3 と 5 を入れてボタンを押す（`add` という機械を動かす）と、`8` というジュース（答え）が出てくる」
- `add(3, 5)` は、この自動販売機と同じ動きをしている

</v-clicks>

</div>

---
layout: center
---

# 4. 一緒に「変身」を追いかけてみよう

次のプログラムを考える。

```js
total = add(1, 2) * 10
```

<v-clicks>

- 「1 と 2 をたす機械に入れて、出てきた答えに 10 をかけて、`total` という箱に入れてね」という意味。
- コンピュータは一気に計算せず、順番に1つずつ「変身」させていく。

</v-clicks>

---

# `total = add(1, 2) * 10` を順番に変身

<div class="grid grid-cols-5 gap-4 items-center mt-4">
<div class="col-span-3 flex flex-col items-center">

````md magic-move {at: 1, lines: true}
```js
total = add(1, 2) * 10
```

```js
total = 3 * 10
```

```js
total = 30
```
````

</div>
<div class="col-span-2 text-sm flex flex-col gap-2">

<div class="p-3 rounded border border-primary/30 bg-primary/5">
<b>①</b> まず <code>add(1, 2)</code> という機械に注目する。
</div>

<div v-click="1" class="p-3 rounded border border-primary/30 bg-primary/5">
<b>②</b> <code>add(1, 2)</code> が変身して <code>3</code> になった。
</div>

<div v-click="2" class="p-3 rounded border border-primary/30 bg-primary/5">
<b>③</b> <code>3 × 10</code> が変身して <code>30</code> になった。
</div>

<div v-click="3" class="p-3 rounded border border-green-500/40 bg-green-500/10">
<b>④</b> <code>30</code> が <code>total</code> という箱にしまわれて計算終了！
</div>

</div>
</div>

<div v-click="4" class="mt-6 p-4 rounded border border-primary/40 bg-primary/10 text-sm">
ポイント：<code>add(1, 2)</code> という機械の答えも、<code>3 + 5</code> のような普通の計算も、<b>「変身して1つの値になる」という点ではまったく同じしくみ</b>。
</div>

---

# 5. 「変身」の考え方は他のところでも使う

### 信号機の例（もしも文）

`もし 信号が青なら → 進む` というプログラムがあったとする。

<div class="grid grid-cols-2 gap-8 items-center mt-4">
<div class="flex justify-center">

<svg viewBox="0 0 200 240" xmlns="http://www.w3.org/2000/svg" class="w-full max-w-48">
  <rect x="60" y="10" width="60" height="140" rx="10" fill="#333"/>
  <circle cx="90" cy="42" r="16" fill="#d33"/>
  <circle cx="90" cy="80" r="16" fill="#dd0" opacity="0.3"/>
  <circle cx="90" cy="118" r="16" fill="#2a5"/>
  <rect x="80" y="150" width="20" height="30" fill="#666"/>

  <text x="90" y="215" text-anchor="middle" style="font-size: 15px; font-weight: bold;" fill="#2a5">真（True）</text>
</svg>

</div>
<div>

<v-clicks>

- 「信号が青かどうか」という部分も実は式で、変身すると `真（True・正しい）` か `偽（False・正しくない）` のどちらかの値になる。

</v-clicks>

<div class="my-4 flex justify-center">

````md magic-move {at: 2, lines: true}
```js
信号が青である
```

```js
真（True）
```
````

</div>

<v-clicks>

- `真（True）` になったときだけ、「進む」が実行される。
- 条件を確かめる部分も、たし算と同じように「変身して答えが出る」としくみが理解できる。

</v-clicks>

</div>
</div>

---

# 機械の中に機械を入れる例

`print(add(1, 2))` というプログラムがあったとする。

<div class="grid grid-cols-2 gap-8 items-center mt-4">
<div class="flex justify-center">

<div class="p-4 rounded-lg border-2 border-blue-400 bg-blue-400/10 text-center">
  <div class="text-sm font-mono font-bold opacity-70 mb-3">print( … )</div>
  <div class="inline-block p-4 rounded-lg border-2 border-orange-400 bg-orange-400/10">
    <div class="text-2xl mb-1">⚙️</div>
    <div class="font-mono font-bold text-sm">add(1, 2)</div>
  </div>
  <div class="text-xs opacity-60 mt-3">内側の機械から先に変身する</div>
</div>

</div>
<div class="flex flex-col items-center">

````md magic-move {lines: true}
```js
print(add(1, 2))
```

```js
print(3)
```

```js
// 画面に 3 と表示される
```
````

<v-clicks class="mt-4 text-sm">

- 先に<strong>内側</strong>の `add(1, 2)` が変身して `3` になる
- そのあとで `print(3)` が実行されて画面に表示される
- 「内側から先に変身する」ルールを覚えよう

</v-clicks>

</div>
</div>

---
layout: center
---

# 6. きょうのまとめ

<v-clicks>

- プログラムの中の「まだ計算していないもの」を<strong>式</strong>という。
- 式が計算されて出てきた「答え」を<strong>値</strong>という。
- 式が値に変身することを<strong>評価</strong>という。
- コンピュータは、式をぜんぶ値に変身し終わるまで、順番に計算を続けている。

</v-clicks>

<div v-click class="mt-8 flex items-center justify-center gap-4">
  <div class="px-6 py-3 rounded-lg border-2 border-blue-400 bg-blue-400/10 font-bold">式</div>
  <div class="text-center text-xs opacity-70">
    <div class="text-2xl leading-none"><carbon:arrow-right /></div>
    評価
  </div>
  <div class="px-6 py-3 rounded-lg border-2 border-orange-400 bg-orange-400/10 font-bold">値</div>
</div>

---

# ミニクイズ

次の式は、最終的にどんな値に変身するか、順番に考えてみよう。

<v-clicks>

1. `2 + 3 * 4` は、まず何を先に変身する？（ヒント：かけ算が先）
2. `add(5, 5) - 2` は、まず何を先に変身する？

</v-clicks>

---

# ミニクイズ：こたえ合わせ

<div class="grid grid-cols-2 gap-10 mt-6">
<div class="flex flex-col items-center">

### 1. `2 + 3 * 4`

````md magic-move {at: 1, lines: true}
```js
2 + 3 * 4
```

```js
2 + 12
```

```js
14
```
````

</div>
<div class="flex flex-col items-center">

### 2. `add(5, 5) - 2`

````md magic-move {at: 3, lines: true}
```js
add(5, 5) - 2
```

```js
10 - 2
```

```js
8
```
````

</div>
</div>

---
layout: center
class: text-center
---

# おつかれさま！

式が値へ「変身」する仕組み＝<strong>評価</strong>をマスターしました。

<PoweredBySlidev mt-10 />
