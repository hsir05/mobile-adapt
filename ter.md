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
