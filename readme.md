#svg入门笔记
- 如果只想展示 SVG 图像的一部分，就要指定viewBox属性
```
<svg width="100" height="100" viewBox="50 50 50 50">//viewBox后参数为左上角的视图横坐
//标和纵坐标 视窗的宽度和高度
  <circle id="mycircle" cx="50" cy="50" r="50" />
</svg>
```
- <circle>标签代表圆形。
<circle>标签的cx、cy、r属性分别为横坐标、纵坐标和半径，单位为像素。坐标都是相对于svg画布的左上角原点。
``` 
<svg width="300" height="180">
  <circle cx="30"  cy="50" r="25" />
  <circle cx="90"  cy="50" r="25" class="red" />
  <circle cx="150" cy="50" r="25" class="fancy" />
</svg>
```
class属性用来指定对应的 CSS 类。
- SVG 的 CSS 属性与网页元素有所不同。
    + fill：填充色
    + stroke：描边色
    + stroke-width：边框宽度
- <line>标签用来绘制直线。
```
<svg width="300" height="180">
  <line x1="0" y1="0" x2="200" y2="0" style="stroke:rgb(0,0,0);stroke-width:5" />
</svg>
```
上面代码中，<line>标签的x1属性和y1属性，表示线段起点的横坐标和纵坐标；x2属性和y2属性，表示线段终点的横坐标和纵坐标；style属性表示线段的样式。
- <polyline>标签用于绘制一根折线。
```
<svg width="300" height="180">
  <polyline points="3,3 30,28 3,53" fill="none" stroke="black" />
</svg>
```
<polyline>的points属性指定了每个端点的坐标，横坐标与纵坐标之间与逗号分隔，点与点之间用空格分隔。
- rect>标签
<rect>标签用于绘制矩形。
<rect>的x属性和y属性，指定了矩形左上角端点的横坐标和纵坐标；width属性和height属性指定了矩形的宽度和高度（单位像素）。
- <ellipse>标签
<ellipse>标签用于绘制椭圆
<ellipse>的cx属性和cy属性，指定了椭圆中心的横坐标和纵坐标（单位像素）；rx属性和ry属性，指定了椭圆横向轴和纵向轴的半径（单位像素）。
- <polygon>标签
<polygon>标签用于绘制多边形
<polygon>的points属性指定了每个端点的坐标，横坐标与纵坐标之间与逗号分隔，点与点之间用空格分隔。
- <path>标签
<path>标签用于制路径。
<path>的d属性表示绘制顺序，它的值是一个长字符串，每个字母表示一个绘制动作，后面跟着坐标。
+ M：移动到（moveto）
+ L：画直线到（lineto）
+ Z：闭合路径
- <text>标签用于绘制文本
<text>的x属性和y属性，表示文本区块基线（baseline）起点的横坐标和纵坐标。文字的样式可以用class或style属性指定。
- <use>标签用于复制一个形状。
<use>的href属性指定所要复制的节点，x属性和y属性是<use>左上角的坐标。另外，还可以指定width和height坐标。