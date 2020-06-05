###### 使用flutter镜像

```
export PUB_HOSTED_URL=https://pub.flutter-io.cn
export FLUTTER_STORAGE_BASE_URL=https://storage.flutter-io.cn
```

###### flutter系统要求

```
操作系统: macOS (64-bit)
磁盘空间: 700 MB (不包括Xcode或Android Studio的磁盘空间）.
工具: Flutter 依赖下面这些命令行工具
			bash, mkdir, rm, git, curl, unzip, which
```

###### 安装flutter sdk

```
拉取代码(Dart SDK已经在捆绑在Flutter里了)
	https://github.com/flutter/flutter.git
	
添加flutter相关工具到path中：
	export PATH=`pwd`/flutter/bin:$PATH
	
运行 flutter doctor
	检查支持flutter的IDE的安装依赖
```

###### flutter启动依赖

```
安装JDK

依赖xcode11-依赖mac(catilina版本)

项目根目录执行，初始化一些项目配置文件
	flutter pub get
```

###### **部署到iOS设备**

```
1.iOS设备
2.CocoaPods依赖关系管理器
3.Apple Developer帐户

安装CocoaPods（ruby写的）
1.使用镜像安装
	gem sources --add https://gems.ruby-china.com/ --remove https://rubygems.org/、
	gem sources -l	查看安装结果，确保只有 gems.ruby-china.com
2.安装CocoaPods
	sudo gem install cocoapods

flutter项目的ios目录中引入第三方依赖(每次修改完成ios记得执行下 flutter clean)
  cd ios	
  pod install --verbose
```

###### 模拟器

```
ios模拟器
	open -a Simulator 打开ios模拟器或者在as中点击图标打开ios模拟器
安卓模拟器
	下载genymotion模拟器（比较耗性能，但是比较流畅）
```

