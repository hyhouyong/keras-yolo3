# keras-yolo3 
![](https://github.com/hyhouyong/keras-yolo3/blob/master/images/images.jpg)
## 一.自定义数据集
    * VOC数据集目录树
      C:.VOCdevkit
              \---VOC2007
                  +---Annotations(使用labelImg保存的标注文件)
                  +---ImageSets
                  |   +---Layout
                  |   \---Main(使用脚本生成test.txt,train.txt,trainval.txt,val.txt)
                  +---JPEGImages(存放所有图片)
                  +---SegmentationClass
                  \---SegmentationObject
   ### 1.安装voc标注工具
    * 本项目使用windows环境下的labelImg
            注意：将图片名字默认6位，eg，000001.jpg
   ### 2.cd到ImageSets下，执行脚本，在Main下生成四个文件
            python test.py
   ### 3.在VOCdevkit的同级目录下执行voc_annotation.py，生成三个txt文件2007_test.txt，2007_train.txt，2007_val.txt
            python voc_annotation.py
   ### 4.将2007_train.txt改为train.txt
## 二.训练
      python train.py
## 三.测试
      python yolo.py
