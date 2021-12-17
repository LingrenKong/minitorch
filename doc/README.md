# Minitorch 练习笔记

<img src="http://minitorch.github.io/_images/minitorch.svg">

这是minitorch的实验笔记

* [Full Guide](http://minitorch.github.io) 

Topics covered:

* Basic Neural Networks and Modules
* Autodifferentiation for Scalars
* Tensors, Views, and Strides
* Parallel Tensor Operations
* GPU / CUDA Programming in NUMBA
* Convolutions and Pooling
* Advanced NN Functions



## 安装

对于extra中的torch包文件，采用了官网的安装指令：

```
pip3 install torch==1.8.2+cpu torchvision==0.9.2+cpu torchaudio===0.8.2 -f https://download.pytorch.org/whl/lts/1.8/torch_lts.html
```

安装后进行测试，却出现问题，网上搜索得知是numba和版本低的问题：

```
import minitorch
... create_target_machine() got an unexpected keyword argument 'jitdebug'
```

升级：

```
 pip install -U numba
```

升级后得到解决
