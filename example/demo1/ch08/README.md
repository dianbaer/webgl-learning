# webgl-learning

根据光源与光线方向，明暗程度不一样并投下影子。
着色：是为了重建光照差生的明暗现象。

光源类型

	平行光 类似于太阳光，因为太阳与地球很远，可以认为是平行的,
		一个方向有一个颜色定义，颜色包含强度
	点光源光 灯泡的光
		点光源会衰减，所以强度会变化。点光源位置与被照射的位置计算。
	环境光 上两种反射出来的光
		各个角度强度都是一致的，不需要指定方向，只需要指定颜色。
	聚光灯光

反射的两个因素：
	入射光与物体表面类型
	入射光含方向与颜色
	物体表面类型含表面固有颜色和反射特性

漫反射
	针对平行光或点光源
	针对粗糙表现非镜子，从不固定的角度反射出去。是均匀的
	《漫反射光颜色》 = 《入射光颜色》*《表面基地色》*cos 0
	入射光与物体法线夹角为0


环境反射

	针对环境光，

	《环境反射光颜色》 = 《入射光颜色》*《表面基底色》



《表面的反射光颜色》 = 《漫反射》+《环境反射》

平行光下的漫反射

	入射角：计算两个矢量的点积
	cos 0 = 《光线方向》`《法线方向》

	《漫反射光颜色》 = 《入射光颜色》*《表面基地色》*（光线方向》`《法线方向》）

	光线与法线矢量长度必须是1

	矢量归一化就是长度为1 每个角度除以矢量长度

	光线方向是光源方向的反方向

法线

cos 0 大于90度说明照射在背面，所有取0

环境光下的漫反射

物体变换，法向量会变化
逆转置矩阵

点光源光










