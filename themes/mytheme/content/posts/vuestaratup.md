+++
title = 'Vue.jsの基本'
date = 2024-03-07T18:08:52+09:00
draft = false
isCJKLanguage = true
tags = ['Webアプリ']
[params]
    subtitle = 'Vue | Vue.js | Webアプリ | Webサイト　Web制作'
+++

##### 目次
* はじめに
* Vue.jsプロジェクト作成コマンド
* Vue.jsの構成
* 処理の記述方法
* まとめ

#### はじめに
Vue.jsでこの[サイト](https://bill.best-book.info "会計.com")を制作したので備忘録として残したいと思います。
金額を入力すると現在カートに入っている商品の金額の合計を表示してくれるサイトです。
今後も様々な機能を追加していく予定です。

#### Vue.jsのプロジェクト作成コマンド
プロジェクトの作成
```bash
npm create vue@latest
cd my-project
npm install
```
サーバーの起動
```bash
npm run dev
```
プロジェクトのビルド
```bash
npm run build
```

#### Vue.jsの構成
```bash
Project
    ├ node_modules
    ├ public                ビルドされたものが出力される
    ├ src
    |   ├ assets            CSSなど
    |   ├ components        componentなど
    |   ├ router            ルーティングの設定
    |   |    └　index.js
    |   ├ views             viewなど
    |   ├ App.vue           これが実際に表示される
    |   └ main.js           App.vueの起動など
    ├ index.html            headなどの記述を書く
    ├ jsconfig.json
    ├ package-lock.json
    ├ package.json
    └ vite.config.js
```

#### 処理の記述方法
コンポーネントのインポートとコンポーネントの配置
```vue
<script>
    import インポートする名前 from 'インポートするファイルの名前'
</script>
<template>
    <インポートする名前 />
</template>
```

値の受け渡し
```vue child.vue
<script setup>
    defineProps({
        msg: {
            type: String,
            required: true
        }
    })
</script>
<template>
    <p>{{ msg }}</p>
</template>
```
```vue parent.vue
<script setup>
    import child from 'child.vue'
</script>
<template>
    <child  msg="こんにちは"/>
</template>

```
ページの移動
```vue
<template>
    <RouterLink to="/">ホーム</RouterLink>
</template>
```
データの定義と処理
```vue
<script>
export default{
    data() {
        return {
            arr : ["1","2"],
            totalPrice : 0,
        }
    },
    methods:{
        func(){
            let a = 1;
            let b = 2;
            let ab = a + b;
            return ab;
        },
        insert(){
            this.arr.push("2");
        },
        change(index){
            this.arr[index] = "10";
        },
    }
}
</script>
<template>
    <p> {{ func() }} </p>                                       <!--更新があるたびに関数を実行する-->
    <button type="button" @click="del(index)">ボタン</button>   <!--ボタンで処理の実行-->
</template>
```

#### まとめ
Vueでサイトを制作する際に必要だったことを主に書いてきました。
次はVue.jsで繰り返しや条件分岐など処理の書き方を投稿したいと思います。