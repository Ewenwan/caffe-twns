# Ternary Weight Networks (TWNs)

This repository implements the benchmarks in our paper "Ternary Weight Networks" which was accepted by the 1st NIPS Workshop on Efficient Methods for Deep Neural Networks (EMDNN), 2016.  

Please cite TWNs in your publications if it helps your research:

    @article{li2016ternary,
      Author = {Li, Fengfu and Zhang, Bo and Liu, Bin},
      Journal = {arXiv preprint arXiv:1605.04711},
      Title = {Ternary Weight Networks},
      Year = {2016}
    }

## Build

Dependencies are identical with the master branch of Caffe. Check out [project site](http://caffe.berkeleyvision.org) for detailed instructions.

NOTE:  
1. Some layers may only have GPU implementation. Thus, CUDA support and GPU devices are required.  
2. The Makefile has been modified to accomodate Ubuntu 16.04. For previous version of Ubuntu, please replace the Makefile with the original one.

## Steps to run a demo  
1. Preparing data  下载minist数据集 
$./data/mnist/get_mnist.sh

        http://yann.lecun.com/exdb/mnist/train-images-idx3-ubyte.gz

        http://yann.lecun.com/exdb/mnist/train-labels-idx1-ubyte.gz

        http://yann.lecun.com/exdb/mnist/t10k-images-idx3-ubyte.gz

        http://yann.lecun.com/exdb/mnist/t10k-labels-idx1-ubyte.gz


    解压：
    gunzip *.gz 或者 gzip -d *.gz  注意解压后没有后缀名

2. Converting data to lmdb   转换成 lmdb 数据库格式
$./examples/mnist/create_mnist.sh


3. Configurations   配置
3.1 setting the PRECISION in the train_lenet_tn.sh  
3.2 setting the DELTA value (0.7 default)  

4. Training         训练
$cd examples/mnist  
$sh train_lenet_tn.sh

5. Run-time usage (to be added)

## Contact

You are welcome to send message to (lifengfu12@mails.ucas.ac.cn) if you have any issue on this code.


