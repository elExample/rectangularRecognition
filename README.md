# 矩形-圆形视觉识别

## 前言


这里提供一种简单的物体形状识别方法，本仓库提供了一个简易的代码去实现。

本仓库是基于 OpenCV 去识别物体的形状

## 应用场景
- 具体看需求，这里并没有实现精度计算

## 逻辑

1. **图像预处理**  
   - 灰度图
   - 高斯模糊减少噪声
   - Canny 边缘检测提取轮廓

2. **轮廓检测**  
   - `cv2.findContours` 方法获取图像中的轮廓。
   - 过滤小噪声轮廓。

3. **形状识别**  
   - 使用 `cv2.approxPolyDP` 简化轮廓点集，判断形状顶点数。
   - 矩形：顶点数为 4，且具有直角。
   - 圆形：通过面积与周长的比值（圆度）判断。

4. **结果标注**  
   - 识别结果。








**引流**: Opencv 矩形识别 | 长方形识别 | 正方形识别 | 圆形识别 | 图像预处理 | 工业工件检测 | 边缘检测 | 工业物体工件检测 | 图像分类


