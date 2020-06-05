###### flutter项目目录结构

```
android——包含Android特定文件的Android子工程
ios——包含iOS特定文件的iOS子工程
build——是运行项目的时候生成的编译文件，即Android和iOS的构建产物
lib——Flutter应用源文件目录，我们自己写的Dart文件都放进lib文件夹中
test——测试文件
pubspec.yaml——管理第三方库及资源的配置文件 
```

###### **Flutter工程的基本架构**

```
lib下的main.dart是flutter的入口文件
main.dart里面的 main 方法是Dart的入口方法
runApp 方法是Flutter的入口方法
```

```
void main() => runApp(MyApp());
组件中build返回一个widget显示界面
@override
  Widget build(BuildContext context) 
```

###### MaterialApp示例

```
MaterialApp用于构建Material设计风格应用的组件封装框架,它封装了应用程序级别的一些Widget。一般作为顶层Widget来使用
常用的属性:
1.home，主页，即应用的首页
2.title，标题
3.color，颜色
4.theme，主题
Scaffold是Material Design布局结构的基本实现,此类提供了用于显示drawer、snackbar和底部sheet的API。
Scaffold有下面几个主要属性：
	1.appBar，显示在界面顶部的一个AppBar，即页面的导航栏
	2.body，当前界面所显示主要内容的widget
	3.drawer，抽屉菜单控件
```

###### 示例

```dart
import 'package:flutter/material.dart';

void main() => runApp(MyApp());

class MyApp extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      color: Colors.red,
      theme: ThemeData.dark(),
      title: "11",
      home: Scaffold(
        drawer: Text("123213"),
        appBar: AppBar(
          title: Text("布局1"),
        ),
        body: Container(
          padding: EdgeInsets.fromLTRB(100, 100, 100, 0),
          child: Row(
            mainAxisAlignment: MainAxisAlignment.spaceEvenly,
            children: <Widget>[
              Row(
                mainAxisSize: MainAxisSize.min,
                children: <Widget>[
                  Icon(
                    Icons.star,
                    color: Colors.red,
                  ),
                  Icon(
                    Icons.star,
                    color: Colors.red,
                  ),
                  Icon(
                    Icons.star,
                    color: Colors.red,
                  ),
                  Icon(
                    Icons.star,
                    color: Colors.grey,
                  ),
                  Icon(
                    Icons.star,
                    color: Colors.grey,
                  ),
                ],
              ),
              Text(
                "评分",
                textAlign: TextAlign.right,
                style: TextStyle(
                    fontSize: 20, letterSpacing: 2.0, color: Colors.blueGrey),
              ),
            ],
          ),
        ),
      ),
    );
  }
}
```