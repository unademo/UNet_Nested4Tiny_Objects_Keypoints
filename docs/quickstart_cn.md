[English](https://github.com/unademo/UNet_Nested4Tiny_Objects_Keypoints/blob/master/docs/quickstart.md) | 中文

## 运行说明

#### 创建热图

- 一张自然原图的目标热图（每张热图上有1个或者多个关键点的信息）数应不大于4（≤ 4）。
- 根据实际物体上这些关键点的内在逻辑关系，组合这些关键点到不同的热图上。
- 在“验证”过程和使用时候的“预测”过程中，前向结果（一些热图）需要被转换成关键点的坐标信息，这个“转换”的方法需要根据创建目标热图时那个逻辑进行编写。
- 如果在“验证过程”没有编写这个方法，会默认进行“最小距离”的自动匹配，即是通过在热图上找到能量最强的n个点，其坐标与目标坐标进行一一比较，总距离最小的方案即为最终匹配结果。根据这个匹配关系，来计算landmark损失值。

#### 运行

- 