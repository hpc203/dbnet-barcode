# dbnet-barcode
使用DBNet检测条形码，
运行程序的依赖库是onnxruntime库，安装方法自行百度

由于onnx文件过大，无法直接上传，我把文件放在百度云盘，
链接: https://pan.baidu.com/s/1mc9X12WyTLSoGQFPwfpyBA  密码: c4d7


在这套程序里，起初我使用opencv读取onnx文件做前向推理，但是输出结果跟onnxrun库的输出不一致，
这也是Pytorch转onnx的一个坑的，详情可以参见我的csdn博客文章 https://blog.csdn.net/nihate/article/details/115504611
