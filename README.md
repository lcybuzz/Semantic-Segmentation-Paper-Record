# Semantic-Segmentation-Paper-Record
主要关注video, weakly supervised, unsupervised等分割方向

# Personal repository under construction

# Table of Contents
- [Video Segmentation](#video-segmentation)
- [Dataset](#dataset)

# Video Segmentation

### OSVOS ★★★
**[Paper]**  (CVPR 2017) One-Shot Video Object Segmentation  <Br>
**[Author]** [Sergi Caelles](https://sergicaelles.com/), [Kevis-Kokitsi Maninis](https://www.kmaninis.com/), [Jordi Pont-Tuset](https://www.kmaninis.com/), [Laura Leal-Taixé](https://dvl.in.tum.de/team/lealtaixe/), [Daniel Cremers](https://vision.in.tum.de/members/cremers), Luc Van Gool<Br>
**[[Project](https://people.ee.ethz.ch/~cvlsegmentation//osvos/)]** **[[Caffe-Code](https://github.com/kmaninis/OSVOS-caffe)]** **[[TF-Code](https://github.com/scaelles/OSVOS-TensorFlow)]** **[[Pytorch-Code](https://github.com/kmaninis/OSVOS-PyTorch)]**<Br>
1) 深度学习做半监督视频分割的首个(?)工作, 场景为分割视频序列中感兴趣目标(2类), 只有第一帧有真值. 未考虑帧间关系, 未考虑实时问题.
2) 首先offline地在图像分割数据集上训练一个前背景两类分割模型, 然后对于给定序列使用第一帧的图像真值对进行online finetune, 另外训练了一个contour预测网络用来refine分割结果. 
  
### agame-vos ★★
**[Paper]**  (CVPR 2019 Oral)  A Generative Appearance Model for End-to-End Video Object Segmentation  <Br>
**[Author]** Joakim Johnander, [Martin Danelljan](https://martin-danelljan.github.io/), Emil Brissman, [Fahad Shahbaz Khan](https://sites.google.com/view/fahadkhans/home), [Michael Felsberg](http://users.isy.liu.se/cvl/mfe/)<Br>
**[[Pytorch-Code](https://github.com/joakimjohnander/agame-vos)]**<Br>
使用GMM对前背景概率进行建模, 在逐帧预测的过程中不断更新均值和方差
  
### STM ★★★
**[Paper]**  (ICCV 2019 Oral)  Video Object Segmentation Using Space-Time Memory Networks <Br>
**[Author]** [Seoung Wug Oh](https://sites.google.com/view/seoungwugoh), [Joon-Young Lee](https://joonyoung-cv.github.io/), [Ning Xu](https://sites.google.com/view/ningxu), [Seon Joo Kim](https://sites.google.com/site/seonjookim/)<Br>
**[[Pytorch-Code](https://github.com/seoungwugoh/STM)]**<Br>
半监督VOS的代表方法, 将之前的预测结果编码为key-value储存起来, 对于当前帧,对其提取特征并作为query与之前帧的key做相似度计算,对value加权取值, 取出的特征和当前特征一并送入decoder预测mask
  
### RGMP
**[Paper]**  (CVPR 2018 Spotlight)  Fast Video Object Segmentation by Reference-Guided Mask Propagation <Br>
**[Author]** [Seoung Wug Oh](https://sites.google.com/view/seoungwugoh), [Joon-Young Lee](https://joonyoung-cv.github.io/), [Kalyan Sunkavalli](http://www.kalyans.org/), [Seon Joo Kim](https://sites.google.com/site/seonjookim/)<Br>
**[[Pytorch-Demo-Code](https://github.com/seoungwugoh/STM)]**<Br> **[[Unofficial-Pytorch-Train-Code](https://github.com/xanderchf/RGMP)]**<Br>

# Dataset
DAVIS [[Page](https://davischallenge.org/index.html)]

YouTube-VOS [[Page](Youtube.com)]

阿里天池视频分割竞赛 [[Page](https://tianchi.aliyun.com/competition/entrance/531797/introduction)]

# Reference
https://github.com/youngryan1993/Video-object-segmentation-paper-list

https://github.com/du0915/Video-Object-Segmentation-Paper-List
