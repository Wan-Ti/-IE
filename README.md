# 兼容-IE

目前在完成一个大屏项目的过程中遇到了兼容IE的需求。发现IE不支持flex布局还不支持echart3.

## 兼容flex布局

```
IE10兼容flex布局的属性使用
IE10以下完全不兼容flex，IE10部分兼容，使用时对应chrome的用法为如下所示：

chrome　　　　　　　　　　　　　　　   IE10

display: flex; 　　　　　　　　　　　　 　display: -ms-flexbox;

flex-direction: column;　　　　　　　　　 -ms-flex-direction: column;

justify-content: center; 　　　　　　　　　-ms-flex-pack: center;

justify-content:space-between;　　　　　  -ms-flex-pack: justify;

justify-content:space-around;　　　　　　 -ms-flex-pack: justify; // 无法实现，用justfiy代替

justify-content: flex-end;　　　　　　　　  -ms-flex-pack: end;

align-items: flex-start;　　　　　　　　　  -ms-flex-align: start;

align-items: center;　　　　　  　　　　　-ms-flex-align: center;

align-items: flex-end;　　　　　　　　　　-ms-flex-align: end;

align-items: baseline;　　　　　　　　　   -ms-flex-align: baseline;

flex: 1;　　　　　　　　　　　　　　　　-ms-flex: 1;
align-self: center;　　　　　 　　　　　　-ms-align-self: center;
flex-wrap: wrap; 　　　　　　　　　　　  -ms-flex-wrap: wrap;
 
注：任何的版本的 Internet Explorer （包括 IE8）都不支持属性值 inherit。
```

## 兼容CSS文本溢出
```
white-space: nowrap;
overflow: hidden;
display: -webkit-box;
text-overflow: ellipsis;
-webkit-line-clamp: 1;
display: -moz-box;
display:block;
-webkit-box-orient: vertical;
-moz-box-orient: vertical;
word-wrap: normal!important;
```

## 兼容内容超出DIV后鼠标滚动
```
-ms-overflow-style: none; /* IE 10+ */
overflow-x: hidden;
overflow-y: auto;
&::-webkit-scrollbar {
   display: none; /* Chrome Safari */
}
```

## Echar2兼容IE

详情看附件



































