# **INS _ CLassify**

这是一个在Tensorflow上建立的CNN图片分类模型，训练和测试的图片均
来自于对Instagram爬虫获得的图片．为了探究CNN深度以及batch norm-
alization对于性能的影响，分别设计了deep model with batch norma-
lization, simple model with batch normalizaion, simple model w-
thout batch normalization三个模型．

- ins _ image _ input.py用于将JPG格式的图片转化为tfrecords文件，
为训练和测试提供图片．
- ins _ train.py用于对模型进行训练，并记录checkpoint
- ins _ eval.py用于对模型进行测试，记录测试时的准确率
- ins _ model.py,ins _ small _ model.py,ins _ small _ model _ bn
分别设计了三种CNN模型用于训练和测试

程序中的函数可以在[Tensorflow](https://www.tensorflow.org/)官网
查找，将图像进行转化和读取可以参考[convert_to_records.py](https://github.com/tensorflow/tensorflow/blob/r1.2/tensorflow/examples/how_tos/reading_data/convert_to_records.py)
以及[fully_connected_reader.py](https://github.com/tensorflow/tensorflow/blob/r1.2/tensorflow/examples/how_tos/reading_data/fully_connected_reader.py).
Tensorflow还有许多详细的[例程](https://github.com/tensorflow/models)可供参考