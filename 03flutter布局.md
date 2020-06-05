Row/Column 常用的属性	Flex 布局

```
1.children → List - 子组件列表
2.mainAxisAlignment → MainAxisAlignment - 主轴对齐方式。
3.crossAxisAlignment → CrossAxisAlignment - 侧轴对齐方式。
4.mainAxisSize → MainAxisSize - 本类的主轴大小。
5.textBaseline → TextBaseline - 基线对齐方式。
6.textDirection → TextDirection - 水平方向上的组件顺序。(左到右还是右到左)
7.verticalDirection → VerticalDirection - 垂直方式上的子组件顺序。(up /down)
8.Row 的宽度由 mainAxisSize 属性确定。如果 mainAxisSize 属性是 MainAxisSize.max，则 - - Row 的宽度是传入约束的最大宽度
根据 mainAxisAlignment（主轴）和 crossAxisAlignment（侧轴）确定每个子组件的位置。

```

###### flex

Column 和 Row 的结合体,只需要设置一下主轴方向就可以变成 Row/Column

```
// 等效于 Column
Flex(
    direction: Axis.vertical,
    children: <Widget>[],
)
// 等效于 Row
Flex(
    direction: Axis.horizontal,
    children: <Widget>[],
)
```

###### flexible

```
Flexible(
    flex: 1,
    fit: FlexFit.loose,
    child: new Text('aaa'),
),
```

###### Expanded

Expanded 与 Flex 类似，但是它会尽可能的扩大，相等于 flex: 1 一样

```
Expanded(
    flex: 1,
    child: Text('aaa'),
),
```

###### center

```
它的尺寸受子组件以及 widthFactor 和 heightFactor 限制,
如果 widthFactor 和 heightFactor 为空着，则 Center 会尽可能大，
如果 widthFactor 是 2.0，那么这个小部件的宽度将总是其子宽度的两倍

child:  Center(
    child:  Column(
        children: <Widget>[
            new Text('Hello'),
        ],
    ),
),
```

###### align

```
Align 是一个对齐布局组件，用于将其子项与其自身对齐，并根据子级的大小自行调整大小
```

###### padding

Padding 是一个带有内边距的布局组件

```
Padding(
    padding: new EdgeInsets.all(8.0),
    child: Card(child: const Text('Hello World!')),
)
```

###### stack

Stack 是一个运允许子组件重叠的布局，类似绝对定位一样

第一个子组件的层次是最低的，之后的逐渐增大，也就是像栈结构一样

```
Stack(
    alignment: Alignment(0.6, 0.6),
    children: <Widget>[
         Text('a'),
         Text('b'),
         Text('c'),
    ]
),
```

###### transform

Transform 是一个动画过渡布局组件

