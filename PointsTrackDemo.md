赛题一：视频特定点位跟踪

视频特定点位跟踪技术常用于视频动态广告植入，如文章开头的动图所示。如果技术足够成熟，观众可能都察觉不到视频中夹杂着广告，也就不会对广告植入产生排斥心理。因此，这种方式可以提升视频平台的变现能力。

但要做出这种「以假乱真」的效果并不容易，算法设计者需要考虑光影、景深、遮挡等各种因素。在此题中，大赛主办方给出了视频片段数据，参赛者需要以此为基础来设计一种有效的植入方案，使得广告自然而然地融入到原始视频中，不对观众产生干扰。

需要强调的是，这道赛题最主要的难点在于如何定位与跟踪。

在跟踪方面，机器之心建议参考深度学习中的视频跟踪类算法，如 SiamMask、SLAM 算法等。

在 SiamMask 中，研究者展示了如何在统一框架下，实时执行视觉追踪与半监督目标分割。在训练完成后，SiamMask 只依赖一个初始化的边界框，就能实时生成未知类别的目标分割掩码，并以每秒 55 帧的速率实时更新掩码。

论文地址：https://arxiv.org/pdf/1812.05050.pdf

![动图封面](simmask.mp4)

SiamMask 的实时分割与追踪效果。
去年 9 月，约克大学的研究者又在 SiamMask 的基础上进行了改进，提出了 SiamMask E，将帧率提高到了 80。

论文地址：https://arxiv.org/pdf/1907.03892.pdf

项目地址：https://github.com/baoxinchen/siammask_e

在视频目标分割方面，大家可以参考悉尼大学等机构的研究者提出的 RANet。

论文地址：https://arxiv.org/pdf/1908.06647.pdf

代码地址：https://github.com/Storife/RANet

另外，大赛出题方还为大家提供了该赛道的官方 demo：https://github.com/MgtvAi/PointsTrackDemo


![影谱科技](http://5b0988e595225.cdn.sohucs.com/images/20190401/4f888ea3d3ae4be9a8858ecb427f93a6.jpeg)
from:  https://sohu.com/a/305151082_751363

References:
- 猫眼对于视频特定点位跟踪问题的解决方案 https://juejin.cn/post/6922775432416886792
- 冠军方案 https://zhuanlan.zhihu.com/p/380903994
- 提画质，插广告，荐视频，“马栏山”杯国际音视频算法大赛怎么拿高分？ https://baijiahao.baidu.com/s?id=1668636848773267141&amp;wfr=spider&amp;for=pc
- The ALOS Dataset for Advert Localization in Outdoor Scenes https://arxiv.org/pdf/1904.07776v1.pdf 
- Identifying Candidate Spaces for Advert Implantation https://arxiv.org/pdf/1910.03227.pdf
- Advertisement Detection and Replacement using Acoustic and Visual Repetition https://static.googleusercontent.com/media/research.google.com/en//pubs/archive/55.pdf
- ADNet: A Deep Network for Detecting Adverts https://arxiv.org/pdf/1811.04115.pdf 
