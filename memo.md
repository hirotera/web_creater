真ん中寄せボタン例

a{
  /* ある種のパターン化されたボタンの構成です */
  display: block;
  width: 336px;
  font-size: 24px;
  font-weight: 700;
  letter-spacing: .075em; /* デザインカンプからテキストの調整 */
  margin-left: 80px;
  line-height: 1;
  color: #fff;
  position: relative;
  text-align: center;
  margin: 80px auto 0 auto;
  padding: 30px 40px;
  text-decoration: none;
  background-color: #FFA41B;
  border-radius: 16px;
  box-shadow: 8px 8px #A96D12; /* フラット型の影では配色の透明度も、ぼかしもないため省略してコードが書ける */
}

# レスポンシブ 
## よく使う感じ
.card {
  box-sizing:border-box;
  width: 280px;
  <!-- borderまでwidthが含まれているのでレスポンシブ対応時のデザイン崩れが起こりづらい -->
  padding: xx 40px;
}

### チェック項目
#### 基本的にコーディング前に全称セレクターにbox-sizing: border-boxを指定しておく
*, *::before, *::after {
  box-sizing:border-box;
}

### 子要素のwidthは指定しすぎない
.parent {
  width: 親要素は指定;
  padding: 40px;
}

.child {
  width: 子要素は指定;
  <!-- 子要素は親要素のpaddingで決まっていく -->
}

## max-width,min-width
max-width:最大幅にしたい値;
min-width:最小の幅にしたい値;

# overflow
## 使い方1
はみ出したくないものを表示させたくない場合､値に[hidden]を入れる
overflow:hidden;

## 使い方2
はみ出したものをスクロールで表示させる
over-flow-x:scroll;

# outlineプロパティ
どこの要素がはみ出しているのか確認しやすくなる
outline:太さ 線の種類 色;
例) outline:2px solid red;

*{
  <!-- 全対称セレクターに入れて目立つ配色にしておく -->
  outline: 3px solid red;
}


# レスポンシブ メディアクエリ
ビューポートの幅によって表示方法を変えること
画面幅=ビューポートではないので注意
<meta name="viewport" 
content="width=device-width, 
initial-scale=1, 
minimum-scale=1, 
maximumscale=1, 
uer-scrable=no">

# CSSにメディアクエリを指定
@media screen and(max-width:768px){
  768px以下はここからの記述が適用される
}