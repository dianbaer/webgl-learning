# webgl-learning

ColoredPoints.js

x = ((x - rect.left) - canvas.width/2)/(canvas.width/2);
y = (canvas.height/2 - (y - rect.top))/(canvas.height/2);

由于坐标系右手坐标系

上、右、外是正方向

RGBA都是从0.0~1.0 不是从0~255

从左到右 -1 0 1
从上到下 1 0 -1

所以((x - rect.left) - canvas.width/2)离中心点的插值
(canvas.height/2 - (y - rect.top))离中心点的插值 相当于-((y - rect.top) - canvas.height/2)