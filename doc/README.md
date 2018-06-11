# MarkdownViewTools

学习springboot时写的一个工具,因为我做接口的经常写文档,改文档,前端每次从svn更新下来很不方便,所以写了一个本地md文档读取展示工具,
前端访问我的ip就能看到相应的文档了


## 现有功能
1. 文档多标签展示
2. toc目录解析
3. 文档上传与下载
4. 文本比较工具

## 如何使用?

1. 使用IDEA clone下来
2. 修改配置文件setting.properties

```
#markdown文件位置
md.mdpath[0] = E://公司/
md.mdpath[1] = /home/web_as/markdown/doc/

#最大获取目录数
md.maxCount=20

#上传临时目录
md.uploadTemppath=E://temp/

#页面缓存url
md.cache[0]=/

#首页欢迎语
md.welecome=#欢迎使用Markdown View Tools
```

3. 使用maven打包为jar
4. 运行java -jar mrdear-1.0.0.jar

项目使用了lombok,如果get和set方法报错,则需要对应IDE安装lombok插件.

## 效果图

1. 总效果图

![1.jpg](http://upload-images.jianshu.io/upload_images/2148449-e22805b5008ef94f.jpg?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

2. 文本比较工具

![2.jpg](http://upload-images.jianshu.io/upload_images/2148449-a2cf45fff3a3b7ce.jpg?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

3. 文档上传

![3.jpg](http://upload-images.jianshu.io/upload_images/2148449-5c846c7315275eed.jpg?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)


## 关于乱码问题
布置的时候有一台全新的linux环境出现乱码问题,查找原因是系统编码不对导致(关于查看,vi一个中文文件,保存后,ls查看,如果会乱码则配置有问题)
解决就是使用`locale -a`查看系统支持的编码,然后`LANG='该编码'`,这里要注意大小写,配置中文UTF-8即可.


## 更新日志

### 2017.11.17
1. 升级Spring Boot版本,作为Spring Boot的入门项目很适合.
2. 修改代码风格,更正之前一些错误的写法.

### 2017.1.18
1. 页面边距调整,目录宽度加大
2. 新增文件删除功能,对目录无效

#### 2016.12.20
1. 前端页面使用layui重新设计
2. 增加多标签显示,很方便的功能
