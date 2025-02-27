---
title: CanvasRenderingContext2D.arc()
slug: Web/API/CanvasRenderingContext2D/arc
---

{{APIRef}}

**`CanvasRenderingContext2D.arc()`** 是 Canvas 2D API 绘制圆弧路径的方法。圆弧路径的圆心在 _(x, y)_ 位置，半径为 _r_ ，根据*anticlockwise* （默认为顺时针）指定的方向从 _startAngle_ 开始绘制，到 _endAngle_ 结束。

## 语法

```
void ctx.arc(x, y, radius, startAngle, endAngle, anticlockwise);
```

### Parameters

- `x`
  - : 圆弧中心（圆心）的 x 轴坐标。
- `y`
  - : 圆弧中心（圆心）的 y 轴坐标。
- `radius`
  - : 圆弧的半径。
- `startAngle`
  - : 圆弧的起始点，x 轴方向开始计算，单位以弧度表示。
- `endAngle`
  - : 圆弧的终点， 单位以弧度表示。
- `anticlockwise` {{optional_inline}}
  - : 可选的{{jsxref("Boolean")}}值 ，如果为 `true`，逆时针绘制圆弧，反之，顺时针绘制。

## 示例

### 使用 `arc` 方法

这是一段绘制圆的简单的代码片段。

#### HTML

```html
<canvas id="canvas"></canvas>
```

#### JavaScript

```js
var canvas = document.getElementById("canvas");
var ctx = canvas.getContext("2d");

ctx.beginPath();
ctx.arc(75, 75, 50, 0, 2 * Math.PI);
ctx.stroke();
```

修改下面的代码并在线查看 canvas 的变化：

```html hidden
<canvas id="canvas" width="400" height="200" class="playable-canvas"></canvas>
<div class="playable-buttons">
  <input id="edit" type="button" value="Edit" />
  <input id="reset" type="button" value="Reset" />
</div>
<textarea id="code" class="playable-code">
ctx.beginPath();
ctx.arc(50, 50, 50, 0, 2 * Math.PI, false);
ctx.stroke();</textarea>
```

```js hidden
var canvas = document.getElementById("canvas");
var ctx = canvas.getContext("2d");
var textarea = document.getElementById("code");
var reset = document.getElementById("reset");
var edit = document.getElementById("edit");
var code = textarea.value;

function drawCanvas() {
  ctx.clearRect(0, 0, canvas.width, canvas.height);
  eval(textarea.value);
}

reset.addEventListener("click", function() {
  textarea.value = code;
  drawCanvas();
});

edit.addEventListener("click", function() {
  textarea.focus();
})

textarea.addEventListener("input", drawCanvas);
window.addEventListener("load", drawCanvas);
```

{{ EmbedLiveSample('Playable_code', 700, 360) }}

### 不同的形状演示

在此例中，使用 arc() 尽可能地绘制不同的形状。

```html hidden
<canvas id="canvas" width="150" height="200"></canvas>
```

```js
var canvas = document.getElementById('canvas');
var ctx = canvas.getContext('2d');

// Draw shapes
for (i=0;i<4;i++){
  for(j=0;j<3;j++){
    ctx.beginPath();
    var x          = 25+j*50;               // x coordinate
    var y          = 25+i*50;               // y coordinate
    var radius     = 20;                    // Arc radius
    var startAngle = 0;                     // Starting point on circle
    var endAngle   = Math.PI+(Math.PI*j)/2; // End point on circle
    var clockwise  = i%2==0 ? false : true; // clockwise or anticlockwise

    ctx.arc(x,y,radius,startAngle,endAngle, clockwise);

    if (i>1){
      ctx.fill();
    } else {
      ctx.stroke();
    }
  }
}
```

{{ EmbedLiveSample('Different_shapes_demonstrated', 160, 210, "https://mdn.mozillademos.org/files/204/Canvas_arc.png") }}

## 规范描述

{{Specifications}}

## 浏览器兼容性

{{Compat}}

## 参见

- 接口定义， {{domxref("CanvasRenderingContext2D")}}
