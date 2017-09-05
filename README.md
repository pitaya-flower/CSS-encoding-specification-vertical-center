#平时写代码遵守的编码规范

1. tab用两个空格表示；
2. ：后加一个空格，{前加一个空格；
3. 每条声明后都要加上分号；
4. 换行,而不是全都放到一行
5. 颜色用小写，用缩写；
6. 小数不用写前缀，0.5->.5，0后不需要加单位;
7. 尽量缩写，margin: 5px 10px 5px 10px;->margin: 5px 10px;

#垂直居中有几种实现方式，给出代码范例
1. 绝对定位实现垂直居中
 ```
<head>
<style>
html,body {
  height: 100%;
}


.dialog {
  position: absolute;
  left: 50%;
  top: 50%;
  margin-left: -200px;
  margin-top: -150px;
  
  width: 400px;
  height: 300px;
  box-shadow: 0px 0px 3px #000;
}

.dialog .header{
  padding: 10px;
  background: #000;
  color: #fff;
}
.dialog .content{
  padding: 10px;
}
</style>
</head>
<body>
  <div class="dialog">
    <div class="header">我是标题</div>
    <div class="content">我是内容</div>
  </div>
</body>
```
2.  vertical align实现垂直居中
```
<head>
<style>
.box{
  width: 300px;
  height: 200px;
  border: 1px solid ;
  text-align: center;
}

.box:before{
  content: '';
  display: inline-block;
  height: 100%;
  vertical-align: middle;
}
.box img{
  vertical-align: middle;
  background: blue;
}
</style>
</head>
<body>
  <div class="box">
    ![](http://upload-images.jianshu.io/upload_images/7279690-8a6eb66fd19c4082.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
  </div>
</body>
```
3. table cell实现垂直居中
 ```
<head>
<style>
.box{
  width: 300px;
  height: 200px;
  border: 1px solid ;
  display: table-cell;
  vertical-align: middle;
  text-align: center;
}
</style>
</head>
<body>
  <div class="box">
    ![](http://upload-images.jianshu.io/upload_images/7279690-8a6eb66fd19c4082.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
  </div>
</body>
```
