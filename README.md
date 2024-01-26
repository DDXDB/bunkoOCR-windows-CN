# bunkoOCR (windows)
findtextCenterNet https://github.com/lithium0003/findtextCenterNet 中公开的机器学习模型，作为应用程序使用的bunkoOCR的Windows版。
这个程序，从图像进行OCR(光学字符识别)，转换成文本。
如果有较新的GPU的话，运行速度会非常快。

## 编译
### 需要
- python
- cmake
- openvino https://docs.openvino.ai/2022.3/openvino_docs_install_guides_installing_openvino_from_archive_windows.html
- CUDA Toolkit 11.8 https://developer.nvidia.com/cuda-11-8-0-download-archive
- cuDNN https://developer.nvidia.com/downloads/compute/cudnn/secure/8.9.5/local_installers/11.x/cudnn-windows-x86_64-8.9.5.29_cuda11-archive.zip/
- TensorRT https://developer.nvidia.com/downloads/compute/machine-learning/tensorrt/secure/8.6.1/zip/TensorRT-8.6.1.6.Windows10.x86_64.cuda-11.8.zip

根据安装的位置，适当修改mak_onnc .bat的路径后运行。

## 运行
运行需要DLL。
- onnxruntime onnxruntime/build/build/Windows/RelWithDebInfo/RelWithDebInfo　
- CUDA Toolkit
- cuDNN
- TensorRT
- openvino runtime/bin/intel64/Release と runtime/3rdparty/tbb/bin 

在运行文件夹中需要有onnx模型。
https://github.com/lithium0003/findtextCenterNet 的Release、下载四个onnx模型并配置。

bunkoOCR.exe是GUI的可执行文件。后台调用OCRengine.exe进行处理。
