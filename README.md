# Atlas200DK_YOLO_V5_CPP


华为Atlas200DK部署运行YOLO_V5_CPP(V6.0前处理用华为的DVPP)

一、环境部署

环境部署分为开发环境和运行环境(此文档为C++版说明)，开发环境为PC端的

ubuntu(16.04验证没有问题)系统环境，运行环境为在Atlas200DK上的环境，具体的环境搭

建可以参考官方说明和网上的相关教程，部分链接地址如下供参考：

https://gitee.com/ascend/samples/tree/v0.3.0/cplusplus/level2_simple_inference/2_object_detection/YOLOV3_coco_detection_picture

https://blog.csdn.net/weixin_44580987/article/details/115704590

过程中遇到的具体问题可以到华为的官方论坛查找或者提问，地址如下：

https://bbs.huaweicloud.com/forum/forum-726-1.html

二、模型转换

1、模型步骤
	
模型转换可参考如下地址的说明：

https://github.com/lenLRX/Atlas_ACL_E2E_Demo/blob/master/yolov5_model_cvt.md

选择的是YOLOV5_v6.0(没有Focus层)版本，所以按照说明可以成功转换模型。

作者对应的中文说明链接如下：

https://zhuanlan.zhihu.com/p/406816839

三、编绎运行代码
	
1、代码链接

本人选择参考的是如下地址的开源代码：

https://github.com/Hanawh/Atlas_200DK_yolov5_cpp

他的中文说明地址如下：

https://blog.csdn.net/qq_36530992/article/details/110264364


2、代码说明

yolov5的v6.0版本没有了FOCUS层的操作所有预处理相对简单(数据预处理的保持宽高比没有实现，这个是不是可以在训练的时间去掉？本人在DVPP未能实现)，

后处理参考华为官方的Samples里的yolov3，然后基于YOLOV5的结果数据解析，推理结果正确。作者的模型转换有点复杂，本人操作也没有成功。


三、测试结果

图像大小：1280*720(720P)

推理网络：yolov5

运行耗时：<40ms(前处理<10ms)



=================================================================================
=================================================================================
说明：代码和工具不是本人源创，都是如下两个开源库作者的贡献

https://github.com/Hanawh/Atlas_200DK_yolov5_cpp

https://github.com/lenLRX/Atlas_ACL_E2E_Demo

再次感谢！！！







