# YOLOV3数据格式

## 1 数据集主要包含两个文件夹

* 文件夹命名
  * train
  * test

## 2 对于train/test文件夹，每一个文件夹又包含了两个文件夹

* train/test文件夹下面各包含两个文件夹
  * images
  * labels
* images文件夹，存放图片文件
* labels文件夹，存放标注文件

## 3 labels文件夹

* 文件格式 txt
* images文件夹中的每一个图片对应一个单独的txt文件
* 在txt文件中，每一行代表一个目标
* 每一行的格式是  **class x_center y_center width height** 一共五个参数
* 标注的**x_center y_center width height** 这四个参数需要归一化到0-1之间。具体就是`x_center` 和 `width` 除以图像宽度， `y_center` 和 `height` 除以图像的高度，参考下图

![avatar](https://user-images.githubusercontent.com/26833433/91506361-c7965000-e886-11ea-8291-c72b98c25eec.jpg)

* 对于**class** 这一个参数，从0开始
* 最终txt的格式参考下图

![avatar](https://user-images.githubusercontent.com/26833433/112467037-d2568c00-8d66-11eb-8796-55402ac0d62f.png)

## 4 images文件夹和labels文件夹

~~~
dataset/images/im0.jpg  # image
dataset/labels/im0.txt  # label
~~~

* images文件夹和labels文件夹下文件的名称应该一样，只是后缀不一样（jpg和txt），进而一一对应

## 5 more

还需要提供类别和数字的对应关系，如0代表人，1代表狗之类的



