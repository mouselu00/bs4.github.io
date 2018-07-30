# bs tutorial
## 目錄
1.  Bootstrap
    -   什麼是Bootstrap（BS）？
    -   為何存在
    -   code
    -   優缺點
    -   其他類似的庫
2. 響應式網頁設計
    -   什麼是RWD
    -   為何存在
3.  版本
    -   遊覽器
    -   BS4 與前版本的差異
    -   解決兼容性的問題
4.  實做
    -   編輯器
    -   下載安裝
    -   基本開始框架


# Bootstrap
##  什麼是Bootstrap（BS）
一個前端元件庫/框架,用於開發 HTML、CSS 和 JS 的開源工具包。以移動裝置為優先設計。

##  為何存在
1.  為了加快前端設計的開發
2.  支援所有遊覽器CSS的文法
3.  有效的提升開發響應時網頁的效率


##  優缺點
優點| 缺點
-|-
開發速度|代碼衝突
簡單易學|代码的规则
视觉效果一致性|视觉效果一致性
對不擅長設計網頁者友好|兼容太早期的版本IE9<需要額外處理
栅格系统|
完善的文檔|

## 其他類似
其他類似BS的還有
-   Foundation Framework
-   Pure CSS
-   Gumby Framework
-   Materialize CSS

#   響應式網頁設計
##  什麼是RWD
無論使用者透過何種裝置瀏覽網頁(包括桌上型電腦、平板電腦或手機)，該網頁一律使用相同的網址和程式碼，只不過網頁的顯示效果會依據螢幕尺寸 進行調整。

##  為何存在
為了滿足用戶在不同大小的熒幕上體驗而規劃出這一套設計概念。

#   版本支援
##  遊覽器
主要大型的遊覽器都支援,但是IE只支援到10+的版本

**Desktop support**
- | chrome | firefox | IE | Edge | opera | safari
-|-|-|-|-|-|-|
WIN|S|S|S>10+|S|S|N
MAC|S|S|N|N|S|S

**Mobile support**
- | chrome | firefox | safari | Android Browser & WebView | Edge
-|-|-|-|-|-|-|
AND|S|S|N|Android 5.0+|S
IOS|S|S|S|N|S
WIN|N|N|N|N|S

##  BS4 與前版本的差異
如果需要把以前使用BS3或更早的版本跟新為BS4，那需要注意的是有些**語法**和樣式已經不再支援或是更新了。建議去翻閱[更新紀錄](http://bootstrap.hexschool.com/docs/4.0/migration/)

##  解決兼容性的問題
方法有很多，例如
-   `<DOCTYPE>`標籤的設定
-   正確呼叫遠端地址
-   針對瀏覽器的內容做標識（使用meta標籤調節瀏覽器的渲染方式）

以上只是部分問題的[解決方案](https://tw.saowen.com/a/9ca6b87d075897ea07b87ef045578fa466b450c58f7eceddc44b387df0bbc079)，更多的資訊可以上網搜尋


#   實做

##  編輯器
-   [codepen](https://codepen.io/)
-   [視覺化開發工具](https://v40.pingendo.com/new)

##   下載安裝
BS4的下載來源有很多
-   [官網](https://getbootstrap.com/docs/4.0/getting-started/download/)
-   [CDN內容傳遞網路](https://www.bootstrapcdn.com/)

##  基本開始框架
1.  表明頁面的類別`<DOCTYPE html>`
```
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="utf-8"> 
  </head>
</html>
```
2.  BS設計的初衷是行動設備優先，影響最大的標籤就是`viewport`
```
<meta name="viewport" content="width=device-width, initial-scale=1">
```
>   `width=device-width` 告訴遊覽器畫面的寬度根據設定的熒幕大小

>   `initial-scale=1` 表示初始化載入畫面時拉進的等級（zoom level）
3.  加入容器`.container`
```
...
<body>
    <div class="container">
    </div>
</body>
...
```
>   `.container-fluid` 是全寬

```
<!doctype html>
<html lang="en">
  <head>
    <!-- Required meta tags -->
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1, shrink-to-fit=no">

    <!-- Bootstrap CSS -->
    <link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/4.0.0/css/bootstrap.min.css" integrity="sha384-Gn5384xqQ1aoWXA+058RXPxPg6fy4IWvTNh0E263XmFcJlSAwiGgFAW/dAiS6JXm" crossorigin="anonymous">

    <title>Hello, world!</title>
  </head>
  <body>
    <div class="container">
        <h1>My First Bootstrap Page</h1>
        <p>This is some text.</p> 
    </div>

    <!-- Optional JavaScript -->
    <!-- jQuery first, then Popper.js, then Bootstrap JS -->
    <script src="https://code.jquery.com/jquery-3.2.1.slim.min.js" integrity="sha384-KJ3o2DKtIkvYIK3UENzmM7KCkRr/rE9/Qpg6aAZGJwFDMVNA/GpGFF93hXpG5KkN" crossorigin="anonymous"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/popper.js/1.12.9/umd/popper.min.js" integrity="sha384-ApNbgh9B+Y1QKtv3Rn7W3mgPxhU9K/ScQsAP7hUibX39j7fakFPskvXusvfa0b4Q" crossorigin="anonymous"></script>
    <script src="https://maxcdn.bootstrapcdn.com/bootstrap/4.0.0/js/bootstrap.min.js" integrity="sha384-JZR6Spejh4U02d8jOt6vLEHfe/JQGiRRSQQxSfFWpi1MquVdAyjUar5+76PVCmYl" crossorigin="anonymous"></script>
  </body>
</html>
```
>   jquery slim版本是3.0之後推出的瘦身版本,當中不包含jquery的AJAX、效果等功能。

>   cdn導入的資源integrity屬性是防止使用期間被串改後導致網崩潰

>   在導入資源的順序很重要

##  BS預設做了什麼
當匯入BS的資源的時候，有些樣式會被BS的樣式設定覆蓋掉。
-   字體預設大小
-   字體樣式
-   列表樣式
-   表格
-   標籤的空間模式（box-sizing）
-   etc

#   核心編碼方式
##  樣式類
BS4都是使用`class`的概念去添加樣式，基本上`id`和`class`最根本的差別就是前者只能是唯一的，後者可以很多。

因為使用`class`所以也能同時給予一個標籤不止一個樣式類

```
//  單一樣式類
<div class="bg-primary"></div>

//  複合樣式類
<div class="bg-primary text-center text-warning"></div>
```
所有的樣式BS4已經寫好讓開發者使用，所以需要找什麼樣式基本上在官方的文檔上都能查詢的到。

>   雖然可以使用`<div>`標籤編輯網頁的排版打天下，但是缺點是會影響SEO的協定

##  樣式使用的順序
一些樣式需要按照原本的順序才可以正常的現實，不然會發生跑版或是無法顯示該有的效果
-   導航樣式類`.nav`
-   表格樣式類`.table`
-   下拉選單樣式類`.dropdown-menu`
-   etc

也有一些樣式類可以不按順序的使用
-   按鈕樣式類`.btn`
-   文本顏色樣式類`.text-primary`
-   背景樣式類`.bg-light`
-   空間調整樣式類`.p-0`
-   etc

#   栅格系统
栅格系统的出現為很多前端開發者在設計排版的時候非常方便而且有效，而他就是響應時設計的主要核型之一。

目前以基礎為目前進行說明  

##  栅格基本概念
一行栅格追多可分成12欄
```
[1][1][1][1][1][1][1][1][1][1][1][1]    =   12
```
以12欄的概念每一欄的大小是1，也可以結合每一欄為4，但總大小一樣不能超過12
```
[4][4][4]   =   12
```
以此類推
【圖：grid system 欄位圖】

##  栅格類
-|Ex small <576px|Small >=576px|Medium >=768px|Large >=992px|Ex large >=120px|
-|-|-|-|-|-|
容器最大寬度|None(auto)|540p|720px|960px|1140px
寫法|`.col-*`|`.col-sm-*`|`.col-md-*`|`.col-lg-*`|`.col-xl-*`|
欄位大小|12
欄位之間空位|30px（個別15px）

## 寫法
`.row`表是行，`.col`表是欄
一行3欄
```
// [] [] [] 
<div class="row">
    <div class="col"></div>
    <div class="col"></div>
    <div class="col"></div>
</div>
```
>   當`.col-*`的設定大小，畫面會自動平均分配寬度

製作一下排版
```
[3][3][3][3]
[4][8]

.row
    .col
    .col
    .col
    .col
.row
    .col-4
    .col-8

```
>   `.col`沒有指定斷點的話是不會更具熒幕大小去變化排版的
```
[3][3][3][3]
[4][8]

.row
    .col-sm
    .col-sm
    .col-sm
    .col-sm
.row
    .col-sm-4
    .col-sm-8
```

##  欄位推移
如果說左右的欄位之間我不需要欄位的存
```
【】 —— 【】
【】【】【】

.row
    .col-md-4
    .com-md-4.offset-md-4
.row
    .col-md-4
    .col-md-4
    .col-md-4
```
>   `.offset-*-*`表是往前移動欄位多少

##  多個斷點
一行內的欄位斷點可以設定多個
```
.col-sm-3.col-md-2
```
>   會檢測md欄位大小=2，sm=3

##  補充
1.  如果不希望欄位之間有空間，可在`.row`上添加`.no-gutters`，會出去掉`margin`和`padding`
2.  在沒有設置寬度的網格欄位將自動以相同寬度佈局。例如，四個 `.col-sm` 將自動設為小中斷點的 25% 寬度,是`flexbox`的功勞。
3.  [更多用法](http://bootstrap.hexschool.com/docs/4.1/layout/grid/)














