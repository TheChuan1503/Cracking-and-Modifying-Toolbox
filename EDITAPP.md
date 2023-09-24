# 修改图标,名字,版本和共存
## 目录
> [修改图标](#icon)
> [修改名字](#name)
> [修改版本](#ver)
> [共存](#gc)
<a id="icon"></a>
## 修改图标
- 把每个/res/mipmap-xdpi里面的ic_launcher.png都换成你自己的图片
![1](img/editapp/1.jpg)
<a id="name"></a>
## 修改名字
###  方法1.修改AndroidManifest.xml中android:label的内容(需要mt的vip或者用np来反编译)
![2](img/editapp/2.jpg)

### 方法2.修改资源属性
1. 复制上图android:label中的内容(不带@)
2. 打开resources.arsc
![3](img/editapp/3.jpg)

3. ID定位资源(输入复制的ID)
![4](img/editapp/4.jpg)

4. 全部替换成你想要改的名字
![5](img/editapp/5.jpg)
<a id="ver"></a>
## 修改版本
1. 打开AndroidManifest.xml
![6](img/editapp/6.jpg)

2. 找到原来的版本名称并修改
![7](img/editapp/7.jpg)
<a id="gc"></a>
## 共存
1. 打开np，找到你要共存的apk
2. 点击功能
3. 点APK共存
