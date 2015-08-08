# webfont
web字体，通过有字库<a href='http://www.youziku.com/' target='_blank'>http://www.youziku.com/</a>提供的web font服务实现web字体功能，给自己的网页增光添彩。
##如何使用
###第一种引用方式，js调用
* js调用。将以下代码添加到您网页的：<head>标签之中，需要说明的是，不同的字体引用的js文件不同，如果需要引用多套字体，那么只需要引用一个js文件即可。
```html
<script type="text/javascript" src="http://www.youziku.com/webfont/FastJS/a58e925547144df997cf5125a36dd507.js"></script>
```
* 设置标签。将以下代码添加到您网页的：</body>标签之后，</html>标签之前，需要说明的是，不同的字体load的后两个参数不一样，详细请查看有字库官网对应字体的参数。这里以迷你简菱心字体为例。
```html
<script  type="text/javascript">
$youziku.load("#id1", "a58e925547144df997cf5125a36dd507", "minijianlinxin");
/*[$youziku.load("#id2", "a58e925547144df997cf5125a36dd507", "minijianlinxin");]*/
/*[$youziku.load(".class1", "a58e925547144df997cf5125a36dd507", "minijianlinxin");]*/
/*[$youziku.load(".class1", "a58e925547144df997cf5125a36dd507", "minijianlinxin");]*/
/*[．．．]*/
$youziku.draw();
</script>
```
    "id1"、"id2"即为要应用字体效果的标签id名字；"class1"、"class2"即为要应用字体效果的标签class名字；粘贴后请自行替换为您页面上真实的标签id或class名字；同一页面上要引用多套字体，只需要将那套字体页面中的应用语句[$youziku.load("xxxxx","xxxxxxxxxxxxxxxxxx","xxxxxxxxxx");]设置在当前应用语句列表之后(．．．的位置)即可。不需要重复引用第一步中的JS文件和[$youziku.draw();]语句。
* 刷新。首次引用此JS代码，有字库需要为新内容生成相应的字体文件，这个过程一般不到一秒，为了保证您能得到好的效果，请您在5s之后刷新一下页面。若内容无变更，即可体验快速推送效果。

###第二种引用方式，css引用
在有字库官网上还提供了一种引用方式，也就是针对特定字生成对应的css引用文件，这样避免了字体文件的全部引用和加载，对于少量使用特定字体的地方适合这样引用。这里使用德彪钢笔行书字体为例。
* 在有字库官网css引用处输入需要使用德彪钢笔行书字体的字，比如：活着就是幸福。
* 之后会生成对应的引用方式说明。
* 在要使用该字体的标签属性中添加如下代码：font-family:LiDeBiao-Xing3397502;或调用class, class="cssb8a5d01058711647d3ea5d61c2c16d5e"
例如：
```html
<h1>调用方式<h1 style="font-family:LiDeBiao-Xing3397502;">
<div>调用方式<div class="cssb8a5d01058711647d3ea5d61c2c16d5e">
```
* 之后是引用方式，分为两种。一种同步方式，一种异步方式。
  * 同步方式（适合少量文本）。
  将以下代码加到你网页的<head>标签之内。
  ```html
  <link href='http://www.youziku.com/webfont/CSS/b8a5d01058711647d3ea5d61c2c16d5e' rel='stylesheet' type='text/css'/>
  ```
  * 异步加载方式（适用于大量文本）。
  将以下代码添加到您网页的</body>标签之后，</html>标签之前。
  ```html
  <script type="text/javascript" src="http://www.youziku.com/UserDownFile/webfont.js"></script> 
  <script type="text/javascript">
    WebFont.load({
        custom: {
            urls: ['http://www.youziku.com/webfont/CSS/b8a5d01058711647d3ea5d61c2c16d5e']
        }
    }); </script>
    ```

##效果展示
* 第一种引用方式效果

![页面效果](https://github.com/RedstoneCMX/webfont/blob/master/showimages/show.png)
![页面效果](https://github.com/RedstoneCMX/webfont/blob/master/showimages/show2.png)
* 第二种引用方式效果

![页面效果](https://github.com/RedstoneCMX/webfont/blob/master/showimages/show3.png)
