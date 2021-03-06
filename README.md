# PPSHITU-image-search
【AI达人创造营第二期】PP-SHITU以图搜图应用(跨镜头搜索)

PP-SHITU以图搜图应用, 本文简单探索了如何用一张参考图片在各个摄像头下快速搜寻它的位置。

**超轻量的主体检测**
主体检测作为整个识别任务的第一步，其本身的精度、性能， 都直接影响整个识别系统的识别效果。PP-ShiTu中使用PP-PicoDet模型作为主体检测算法，PP-PicoDet模型性能和速度均达到业内SOTA的水平，为整个识别系统实现精准高效识别打下了坚实的基础。

**高效的特征提取模块**
图像识别的又一大问题就是如何让模型提取到更好的特征。在特征提取的训练阶段，PP-ShiTu通过使用度量学习，更好地解决高相似度物体的区分问题。不仅如此，PP-ShiTu所使用的骨干网络PP-LCNet作为业内SOTA模型，大幅度提升预测速度的同时，还提高了精度，并且可能直接支持多种应用方向和场景，真节省开发成本的一把好手!

**快速向量检索支持**
在实际应用中，海量的图像、视频特征不仅会消耗巨大的存储空间，而且检索时间极长，给图像识别的最后一公里设下路障。PP-ShiTu则是结合DeepHash和度量学习，甚至在检索库特征数量大于10万时，依然使得所需的存储空间减少32倍，检索速度提高5倍以上。除此以外PP-ShiTu使用的向量搜索模块Faiss，可以更好地适应多平台的需求(Linux, Windows, MacOs)，为实际应用提供灵活选择。
这样一个高效系统使用起来却只需三步，绝对的”开箱即用”！
