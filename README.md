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
  
### agame-vos
**[Paper]**  (CVPR 2019)  A Generative Appearance Model for End-to-End Video Object Segmentation  <Br>
**[Author]** Joakim Johnander, [Martin Danelljan](https://martin-danelljan.github.io/), Emil Brissman, [Fahad Shahbaz Khan](https://sites.google.com/view/fahadkhans/home), [Michael Felsberg](http://users.isy.liu.se/cvl/mfe/)<Br>
**[[Pytorch-Code](https://github.com/joakimjohnander/agame-vos)]**<Br>
  
### STM
**[Paper]**  (ICCV 2019)  Video Object Segmentation Using Space-Time Memory Networks <Br>
**[Author]** [Seoung Wug Oh](https://sites.google.com/view/seoungwugoh), [Joon-Young Lee](https://joonyoung-cv.github.io/), [Ning Xu](https://sites.google.com/view/ningxu), [Seon Joo Kim](https://sites.google.com/site/seonjookim/)<Br>
**[[Pytorch-Code](https://github.com/seoungwugoh/STM)]**<Br>

# Dataset
Davis **[[Project](https://davischallenge.org/index.html)]**
