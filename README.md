NVIDIA社のGPUを積んだPCが必要。
ドライバーとCUDAがインストールされている場合は以下のように出力される。

$nvidia-smi
Thu Aug  5 22:36:16 2021       
+-----------------------------------------------------------------------------+
| NVIDIA-SMI 460.91.03    Driver Version: 460.91.03    CUDA Version: 11.2     |
|-------------------------------+----------------------+----------------------+
| GPU  Name        Persistence-M| Bus-Id        Disp.A | Volatile Uncorr. ECC |
| Fan  Temp  Perf  Pwr:Usage/Cap|         Memory-Usage | GPU-Util  Compute M. |
|                               |                      |               MIG M. |
|===============================+======================+======================|
|   0  GeForce GTX 1070    Off  | 00000000:09:00.0 Off |                  N/A |
|  0%   45C    P8     8W / 180W |    352MiB /  8116MiB |      0%      Default |
|                               |                      |                  N/A |
+-------------------------------+----------------------+----------------------+
                                                                               
+-----------------------------------------------------------------------------+
| Processes:                                                                  |
|  GPU   GI   CI        PID   Type   Process name                  GPU Memory |
|        ID   ID                                                   Usage      |
|=============================================================================|
|    0   N/A  N/A      1250      G   /usr/lib/xorg/Xorg                 18MiB |
|    0   N/A  N/A      1417      G   /usr/bin/gnome-shell               73MiB |
|    0   N/A  N/A      2305      G   /usr/lib/xorg/Xorg                199MiB |
|    0   N/A  N/A      2438      G   /usr/bin/gnome-shell               27MiB |
|    0   N/A  N/A      2904      G   ...AAAAAAAAA= --shared-files       27MiB |
+-----------------------------------------------------------------------------+

##Jupyter Notebookでの実行方法

[CPU]
'''
inPath = "test.jpg"
outPath = "test_cpuout.jpg"
blackWhite(inPath , outPath , mode = "luminosity",log = 1)
'''

[GPU]
'''
inPath = "test.jpg"
outPath = "test_gpuout.jpg"
CudablackWhite(inPath , outPath , mode = "luminosity" , log = 1)
'''


