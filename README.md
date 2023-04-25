# iOSOpenDev_Specifications
记录一份iOSOpenDev补丁

iOSOpenDev是一个开源项目，它可以设置iOS SDK以允许在Xcode中进行开放式开发，以构建不受默认支持或允许的越狱类型项目，并提供用于构建常见越狱类型项目和所需工具的Xcode模板。

[iOSOpenDev官网下载](http://iosopendev.com/download/)

看到更新到1.6-2,但是是2013年的,目前已经10年没更新了,听说作者不写了.

直接安装的话会提示失败

<img width="357" alt="image" src="https://user-images.githubusercontent.com/4438229/233945272-c94c23cd-ccf5-4872-9cea-b43774465ed1.png">


* iPhoneOS开头的文件放 `/应用程序/Xcode/Content/Developer/Platforms/IphoneOS.platform/Developer/Library/Xcode/Specifications` 文件夹下（如无自建）
* iPhone Simulator开头的文件放 `/应用程序/Xcode/Content/Developer/Platforms/iPhoneSimulator.platform/Developer/Library/Xcode/Specifications` 文件夹下(如无自建)
* 在 `/应用程序/Xcode/Content/Developer/Platforms/iPhoneSimulator.platform/Developer/` 文件夹下创建usr文件夹，usr文件夹下再创建一个名为bin的文件夹

打开Xcode创建新项目,在iOS分类下,最下面会看到iOSOpenDev的模版.


# 诡异的事情

以上修改问题,只是为了能将iOSOpenDev工具顺利安装,但是安装之后,我的Xcode创建的iOS项目,会隐藏掉"Signing & Capabilities"

我将以上2个Specifications文件夹删掉了,经过测试并不影响创建插件项目.并且"Signing & Capabilities"又显示出来了
