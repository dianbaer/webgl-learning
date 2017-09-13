# webgl-learning

gl.TRIANGLE_STRIP(v0 v1 v2),(v1 v2 v3)

gl.TRIANGLE_FAN(v0 v1 v2),(v0 v2 v3)

gl.TRIANGLES(v0 v1 v2),(v3 v4 v5)少于三个忽略

gl.LINE_LOOP(v0 v1),(v1 v2),(v2 v0)

gl.LINE_STRIP(v0 v1),(v1 v2)

gl.LINES(v0 v1),(v2 v3)少于2个忽略

gl.POINTS画点

创建缓冲区-》绑定-》绑定数据-》绑定方式-》激活

如果平移xyzw最后的w参数需要设置为0.0
平移是xyzx各点相加
旋转：旋转轴 旋转方向 旋转角度

正旋转：绕z轴逆时针

x=r cos a
y=r sin a

x1 = r cos(a+b)
y1 = r sin(a+b)

三角函数两角和公式

sin(a+-b) = sin a cos b -+ cos a sin b

cos(a+-b) = cos a cos b -+ sin a sin b

带入得

x1 = r(cos a cos b - sin a sin b)
y1 = r(sin a cos b + cos a sin b)

最终
x1 = x cos b - y sin b
y1 = x sin b + y cos b

角度转弧度

Math.PI*ANGLE/180.0






