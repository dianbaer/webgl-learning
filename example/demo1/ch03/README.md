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

变换矩阵 旋转
矩阵乘法不符合交换律，a*b与b*a不相等

x1   a  b  c   x
y1 = d  e  f * y
z1   g  h  i   z

x1 = ax + by + cz
y1 = dx + ey + fz
z1 = gx + hy + iz

这样设置，这个进行了一次旋转，所以叫旋转矩阵 rotation matrix
x1   cosb  -sinb 0   x
y1 = sinb  cosb  0 * y
z1   0      0    1   z

就完全等于

x1 = x cos b - y sin b
y1 = x sin b + y cos b

变换矩阵 平移

平移需要4*4矩阵

x1   a b c d   x
y1   e f g h   y
   =         *
z1   i j k l   z
1    m n o p   1

x1 = ax + by + cz + d
y1 = ex + fy + gz + h
z1 = ix + jy + kz + l
1  = mx + ny + oz + p

推出平移矩阵

x1   1 0 0 Tx   x
y1   0 1 0 Ty   y
   =         *
z1   0 0 1 Tz   z
1    0 0 0 1    1


4*4旋转矩阵

x1   cosb  -sinb 0 0   x
y1 = sinb  cosb  0 0 * y
z1   0      0    1 0   z
1    0      0    0 1   1

一维数据存储矩阵分为按行按列两种
默认是按列主序

矩阵乘法不可逆
gl_Position = u_xformMatrix * a_Position

变换矩阵 缩放

x1   Sx 0  0  0   x
y1 = 0  Sy 0  0 * y
z1   0  0  Sz 0   z
1    0  0  0  1   1








