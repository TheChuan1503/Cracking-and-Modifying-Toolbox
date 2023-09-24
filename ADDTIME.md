# 加时教程
## 目录
> [手动加时](#sdjs)
> [自动加时](#zdjs)
<a id="sdjs"></a>
## ◎手动加时
### 添加addtime函数
1. 打开activity记录
![activity记录](img/addtime/1.jpg)

2. 进入游戏并记录activity名称
![进入游戏](img/addtime/2.jpg)
![记录activity](img/addtime/3.jpg)

3. 编辑dex
![3.1](img/addtime/4.jpg)
![3.2](img/addtime/5.jpg)

- 下面的 "**d21**" 是你记录的activity名字
![3.3](img/addtime/6.jpg)
![3.4](img/addtime/7.jpg)
![3.5](img/addtime/8.jpg)
![3.6](img/addtime/9.jpg)

- 在最下面写这段代码
  ```java
  .method public addtime(Landroid/view/View;)V
      .registers 3
  
      invoke-static {}, {sign}
  
      return-void
  .end method
  ```
- 把{sign}替换成你复制的方法签名
![添加addtime函数](img/addtime/10.jpg)

- 保存并退出
### 反资源混淆
- 打开**NP管理器**
- 找到apk文件
- 打开，点功能，点RES反资源混淆
![1](img/addtime/11.jpg)

### 添加加时按钮
- 回到MT
1. 打开ui的xml文件
![1.1](img/addtime/12.jpg)

- /res/layout-v21/toolbox_overlay.xml
![1.2](img/addtime/13.jpg)

2. 反编译
![2.1](img/addtime/14.jpg)

3. 在指定位置写入下面这段代码
  ```xml
    <ImageView
                android:background="@7F08011F"
                android:layout_width="-2"
                android:layout_height="-2"
                android:layout_marginBottom="16dp"
                android:src="@7F080097"
                android:onClick="addtime"
                app:tint="#FFFFFFFF" />
  ```
- 如图
- 
  ![2.2](img/addtime/15.jpg)
  
4. 保存并退出
![4.1](img/addtime/16.jpg)

5. 安装并打开
![5.1](img/addtime/17.jpg)

6. 可以加时了
![5.2](img/addtime/18.jpg)
----
<a id="zdjs"></a>
## ◎自动加时
### 获取加时代码
1. 记录activity名称
2. 打开dex搜索类名并找到方法g
- 以上请见[手动加时](#sdjs)
3. 复制代码下图中的代码(就是方法g里面的代码)
![3.1](img/addtime/a1.jpg)

4. 搜索字符串internal/premium/remaining_time
![4.1](img/addtime/a2.jpg)

5. 搜索结果一个一个去看(或直接在结果中搜索方法a)，直到找到方法名是a的(就像下面的)
![5.1](img/addtime/a3.jpg)
![5.2](img/addtime/a4.jpg)

6. 如图，删掉绿色横线里面原来的内容，替换成第3步复制的代码
![6.1](img/addtime/a5.jpg)

7. 如图，找到MinecraftActivity，并添加第3步的代码
![7.1](img/addtime/a6.jpg)
![7.2](img/addtime/a7.jpg)

- 在方法onCreate开头添加代码
![7.3](img/addtime/a8.jpg)

8. 保存并退出
9. 安装并打开
10. 可以自动加时了
![autoaddtime](img/addtime/a9.jpg)
