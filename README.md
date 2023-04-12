# html css Tutorial
 
# HTML
一個基本的 HTML 格式。
(用 VS Code 開新檔案，格式選擇 HTML 後，輸入一個驚嘆號+Enter)

需另存為 index.html

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>[標題]</title>
</head>
<body>
    [這邊放網站內容]
</body>
</html>
```


## 常見 HTML 標籤

### 標題 h1~16
```html
<h1>第一級標題</h1>
<h2>第二級標題</h2>
<h6>第六級標題</h6>
```
### 段落
```html
<p>段落內容.....</p>
<p>段落內容.....</p>
```
### 圖片 img
(不用結束標籤)
```html
<img src="圖片檔名">
```

### 連結 a
```html
<a href="網址">要連結的內容</a>
<a href="網址" target="_blank">開新分頁的連結</a>
```

### div 標籤
每組 HTML div 標籤都是一個區塊元素，一次占用掉一整行的空間，
每個區塊內還可以增加更小的區塊，有利於進行排版。
```html
<div>內容.....</div>
```

### 母子關係
可精簡程式碼，可在style裡讓小孩設定跟隨媽媽。
```css
（媽媽） > （小孩）
例:
.circle(媽媽) { width:10px }
.circle > .img { width:100% }（寬度跟隨媽媽）
```

### class代號名稱
加在標籤後，用代名稱號標識特定的標籤。
```html
<p class="代號名稱"> 內容 </p>
<div class="代號名稱"> 內容 </div>
<img class="代號名稱" src="aaa.png"/>
```



# Style
用來設定 HTML 文件的樣式
```html
<style>
.代號名稱 { CSS樣式... } 
</style>
*** 注意名稱前的 "." 要記得打 ***
```

## CSS 常用樣式
### 文字類
```css
color: red;                     /* 文字顏色 (也可以用色碼) */ 
font-size: 10pt;                /* 文字大小 (單位通常用pt) */
font-family: sans-serif;        /* 文字字型 (無-襯線) */
text-align: center;             /* 文字對齊 */
font-weight: 100;               /* 文字粗細 (不需單位)*/
(normal | bold | 100-900)          
(  預設  | 粗體  |以數字設定（100為單位) )
```
### 裝飾類
```css
background-color: red;          /* 背景顏色 (也可以用色碼) */ 
border-radius: 20pt;            /* 圓角 （值越大越圓）*/
box-shadow: 0px 15px 40px red;  /* 陰影（x y 模糊程度 顏色）*/
border: solid 1px red;          /* 邊框（樣式 粗細 顏色 ）*/
/*solid、double、dotted、dashed    實線、雙實線、虛線、點點 */
```

### 排版類
```css 
display: block;                           /* 顯示型態 */
block | inline ｜ inline-blockblock
( 區塊 |  行內   | 以inline的方式呈現，但同時擁有block的屬性 ）                  

display: flex;                            /* 隨著網頁縮放改變比例 */
(需先設成flex，底下語法才可使用)

justify-content:                          /* 水平對齊 */
flex-start | flex-end | center | space-between
(   置前    ｜    置後  ｜  置中  ｜  均分  )

align-item:                               /* 垂直對齊 */
flex-start | flex-end | center 
(   置前    ｜    置後  ｜  置中   )

flex-wrap:                                /* 換行設定 */
 nowrap | wrap | wrap-reverse;
 (預設值 ｜ 換行 ｜ 換行，且行順序反轉 )



padding:                                  /* 內距 (數值寫法) */
 12px 0 0 0/ 10px 12px/ 0 12px 0/    12px;
(上 右 下 左/ 上下  左右 / 上 左右 下/ 四邊同樣値;)

padding-top/ right/ bottom/ left: 12px;   /* 內距 (標籤寫法) */
      ( 上方/ 右方 /  下方 / 左方的內距 )
      
margin:                                   /* 外距 (數值寫法) */
 12px 0 0 0/ 10px 12px/ 0 12px 0/    12px;
(上 右 下 左/ 上下  左右 / 上 左右 下/ 四邊同樣値;)
                                        
margin-top/ right/ bottom/ left: 12px;    /* 外距 (標籤寫法) */
      ( 上方/ 右方 /  下方 / 左方的內距 )

```

## 元素位置 Position
```css
relative                     /* 移改變，但原位置保留 */
(搭配top/left參數 ) 

absolute                     /* 位置被忽視，可自由在網頁上任何地方 */
(自動向上尋找有position設定的元素跟著，寬度高度等細節需手動設定)

fixed                        /* 位置浮動對齊螢幕 */
(搭配top/bottom/left/right參數 ) 
```


## 引入共用CSS
若HTML有相同CSS內容，可引入共用的CSS檔案
```css
先將CSS內容單獨存檔（存css檔）
刪除整個 <style> 區
改輸入 <link href="檔名.css" rel="stylesheet"> 
```