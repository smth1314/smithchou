# 我的项目文件夹

## 目录结构

```text
  + assets                资源文件夹(第三方资源)
    - jquery
    - bootstrap
    - jquery-pageination
    - jquery-validation
  + font                  项目需要用到的 矢量图标 文件(第三方资源)
    - demo.css
    - iconfont.css
    - iconfont.eot
    - iconfont.js
    - iconfont.json
    - iconfont.svg
    - iconfont.ttf
    - iconfont.woff
    - iconfont.wpff2
  + css                   项目需要用到的 css 文件
    -  index.css
    - cart.css
    - detail.css
    - list.css
    - logion.css
    - public.css
  + images                项目需要用到的 图片 文件
    - ￥0.png
    - duo.png
    - find.png
    - hao.png
    - kuai.png
    - last.png
    - logins_01.png
    - logins_02.png
    - logo.png
    - logo.png
    - lunbo1.png
    - lunbo2.png
    - luobo3.png
    - luobo4.png
    - luobo5.png
    - luobo6.png
    - luobo7.png
    - luobo8.png
    - luobo9.png
  + js                    项目需要用到的 js 文件
    - banner.js
    - big.js
    - cart.js
    - detail.js
    - form.js
    - index.js
    - list.js
    - list2.js
    - login.js
    - public.js
  + server                项目需要用到的 后端 书写
    - getCateOne.php
    - getCateThree.php
    - getCateTwo.php
    - getGoodInfo.php
    - getGoodList.php
    - getTotaPage.php
    - login.php
  - index.html            首页
  - cart.html             购物车页面
  - detail.html           商品详情页面
  - list.html             商品列表页面
  - login.html            登录页面
```


## 导入数据库
+ 打开 mysql 可视化工具
    - 新建一个 `database` 叫做 `bk2004`
    - 导入 `goods.sql` 的文件
+ 创建表格
    - 新建一个表格, 叫做 `user`
    - 创建用户信息
      => user_id: 1   username: admin   password: 123456   nickname: 管理员
      => user_id: 2   username: wangyu  password: 223322   nickname: 王瑜


## 配置站点域名
+ 配置一个站点域名
    - www.zhoumi.com / zhoumi.com

## index.html 页面布局 和 功能的实现
+ 页面头部
    - 登录按钮,  用户登录信息
+ 搜索引擎
    - 使用 百度的数据
    - 根据文本框内容发送 jsonp 请求, 接收后端数据
    - 根据返回的数据渲染页面
+ 轮播图区域
    - 渐隐渐现轮播图
    - 进入页面, 开启自动轮播
    - 点击焦点, 可任意切换图片
    - 点击左右按钮, 可向左或向右切换图片
    - 当鼠标移入, 暂停轮播
    - 当鼠标移出, 再次开启轮播
+ 购物车按钮
    - 点击 购物车 按钮, 可跳转 购物车 页面
+ 列表分类区域
    - 点击 列表分类 的内容, 可跳转 商品列表 页面


## login.html 页面布局 和 功能的实现
+ 登录窗口
    - 点击登录按钮, 获取后端数据
      => 进行表单验证
      => 验证通过后, 跳转首页


## list.html 页面布局 和 功能的实现
+ 筛选区域
    - 通过发送 jsonp 请求, 就收后端数据
    - 根据返回的数据来渲染 筛选信息 分页信息 和 列表信息
    - 点击 一级分类
      => 获取 二级分类 和 列表信息
    - 点击 排序方式
      => 可实现 价格 销量 正序或者倒序的切换
+ 分页信息区域
    - 通过后端返回的数据来渲染 分页信息
    - 点击 数字按钮 可切换对应的页面
    - 点击 左右按钮 可切换上一页或下一页
+ 列表信息区域
    - 根据后端返回的数据来渲染 列表信息
    - 点击商品名称, 可进入 列表详情
    - 点击 加入购物车按钮, 可将 一件此商品 加入购物车
    - 点击 去结算按钮, 可进入 购物车界面


## detail.html 页面布局 和 功能的实现
+ 渲染页面
    - 通过后端返回的数据
    - 渲染商品详细信息
    - 商品图片
    - 商品描述
    - 商品价格
    - 商品详细信息
+ 放大镜效果
    - 将鼠标移动至大图区域
    - 右侧处出现放大效果图
    - 通过鼠标移动在大图区域的移动
    - 控制放大镜盒子背景图片的移动范围
+ 添加商品数量文本框
    - 可通过手动输入所需商品数量
    - 也可以通过 '+' '-' 来增加或减少商品数量
+ 加入购物车
    - 点击加入购物车按钮
    - 可添加对应文本框的 该商品的数量


## cart.html 页面布局 和 功能的实现
+ 无商品
    - 可点击 现在去选购按钮, 进入 商品列表页面
+ 有商品
    - 点击选项框, 选择需要结算的商品
    - 会计算出所有商品的数量, 及商品的价格
    - 点击 删除 按钮
    - 可删除该商品