# Land-use Classification of Remote Sensing

## 教程使用

教程中的样例展示文件是 predict.ipynb，运行这个文件，会安装环境，并展示已有模型的识别效果。

### 项目路径

* 测试图片路径：semantic_pytorch/out/result/pic3
* 掩膜图片路径：semantic_pytorch/out/result/label
* 预测图片路径：semantic_pytorch/out/result/predict
* 训练数据列表：train.csv
* 测试数据列表：test.csv

## 使用说明

训练模型进入 semantic_pytorch，训练的模型被保存在 model/new_deeplabv3_cc.pt。
模型采用 DeepLabV3plus，训练参数中，Loss 采用二进制交叉熵。Epoch 为600，初始学习率0.05。

训练指令：

```sh
python main.py
```

如果使用我们已经训练好的模型，则使用保存在 model 文件夹中 fix_deeplab_v3_cc.pt，在 predict.py 中直接调用即可。

预测指令：

```sh
python predict.py
```



