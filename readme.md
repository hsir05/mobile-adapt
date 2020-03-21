# 移动端适配方案

## 1. rem布局

首先确定你的设计稿是基于iphone6还是iphone4/5：

如果设计稿基于iphone6，横向分辨率为750，body的width为750 / 100 = 7.5rem

如果设计稿基于iphone4/5，横向分辨率为640，body的width为640 / 100 = 6.4rem

1. 对视口做如下设置：

    `<meta name="viewport" content="initial-scale=1,maximum-scale=1, minimum-scale=1">`

2. 在index.html入口文件里写：

```javascript
var deviceWidth = document.documentElement.clientWidth;

document.documentElement.style.fontSize = deviceWidth / 6.4 + 'px';  // 注意：iphone6要除以7.5
```

## 2. media实现rem适配

根目录设置`html{ font-size:16px}`
长度单位都用`rem`设置

```css
@media screen and (min-width: 320px) {html{font-size:50px;}}
@media screen and (min-width: 360px) {html{font-size:56.25px;}}
@media screen and (min-width: 375px) {html{font-size:58.59375px;}}
@media screen and (min-width: 400px) {html{font-size:62.5px;}}
@media screen and (min-width: 414px) {html{font-size:64.6875px;}}
@media screen and (min-width: 440px) {html{font-size:68.75px;}}
@media screen and (min-width: 480px) {html{font-size:75px;}}
@media screen and (min-width: 520px) {html{font-size:81.25px;}}
@media screen and (min-width: 560px) {html{font-size:87.5px;}}
@media screen and (min-width: 600px) {html{font-size:93.75px;}}
@media screen and (min-width: 640px) {html{font-size:100px;}}
@media screen and (min-width: 680px) {html{font-size:106.25px;}}
@media screen and (min-width: 720px) {html{font-size:112.5px;}}
@media screen and (min-width: 760px) {html{font-size:118.75px;}}
@media screen and (min-width: 800px) {html{font-size:125px;}}
@media screen and (min-width: 960px) {html{font-size:150px;}}
```