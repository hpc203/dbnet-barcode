# dbnet-barcode
使用DBNet检测条形码，
运行程序的依赖库是onnxruntime库，安装方法自行百度

由于onnx文件过大，无法直接上传，我把文件放在百度云盘，
链接: https://pan.baidu.com/s/1mc9X12WyTLSoGQFPwfpyBA  密码: c4d7


在这套程序里，起初我使用opencv读取onnx文件做前向推理，但是输出结果跟onnxrun库的输出不一致，
这也是Pytorch转onnx的一个坑的，详情可以参见我的csdn博客文章 https://blog.csdn.net/nihate/article/details/115504611

5月28日，添加了C++版本的程序，由于在python程序里验证了使用opencv检测条形码的结果错误，
因此在C++版本的程序里选择onnxruntime库作为推理框架，程序已经在ubuntu系统调试运行通过。
如果你想运行程序，需要先从微软的github仓库里下载已经编译过的onnxruntime库的压缩包，解压到本地后，打开
CMakeLists.txt，修改onnxruntime库的路径和版本为你的本机上的onnxruntime库，然后在clion环境里编译运行。
由于我是使用onnxruntime库没多久，没有在windows10系统里做过onnxruntime库的程序开发。因此，读者
如果想在windows10系统运行程序，需要修改CMakeLists.txt
