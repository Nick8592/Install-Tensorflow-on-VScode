# Install-Tensorflow-on-VScode
## Follow the Steps Below

- **Download Python**  
(http://python.org/downloads/)  
make sure to tick the checkbox “Add Python 3.xx to PATH”  

- **Open “Command Prompt 命令提示字元”, and type in**
    
    ```python
    python --version
    ```
    >(Should pops up >> Python 3.xx <-----version you download)
    
    ```python
    python -m pip install --upgrade pip
    ```
    
    ```python
    pip install matplotlib
    ```
    
- **Search your CUDA version for your graphic card**  
(https://forums.developer.nvidia.com/t/cuda-10-1-and-gtx-1660-ti-not-compatible/79704)  
e.g. RTX 1660Ti >>> CUDA toolkit 10.x 
(but we download newer version CUDA toolkit 11.0) 

- **Check CUDA / Microsoft Visual C++ compatibility**  
(https://quasar.ugent.be/files/doc/cuda-msvc-compatibility.html)   
e.g. CUDA 11.0 >>> Visual C++ 2017

- **Download Visual Studio**  
(https://visualstudio.microsoft.com/zh-hant/vs/older-downloads/)

- **Decide Tensorflow version, and see its cuDNN & CUDA requirments.**  
(https://www.tensorflow.org/install/source)  
e.g. tensorflow-2.5.0 >>> cuDNN 8.1, CUDA 11.2

- **Go to NVIDIA CUDA site download corresponding CUDA version**  
(https://developer.nvidia.com/cuda-toolkit-archive)  
e.g. CUDA Toolkit 11.2.0

- **Go to NVIDIA cucDNN site download corresponding cuDNN version**  
(https://developer.nvidia.com/cudnn)  
e.g. cuDNN v8.1.0 (January 26th, 2021), for CUDA 11.0,11.1 and 11.2

    >Extract the “cudnn" file, and copy “bin, include, lib” folders into local folder,   
    locate at somewhere like “C:\Program Files\NVIDIA GPU Computing Toolkit\CUDA\v11.2”. 
    >>Search “Edit the system environment variables 檢視進階系統設定”, click right-bottom “”Environment Variables 環境變數..."  
    >>>Double click “Path” at User variable for xxx.  
    >>>>Copy “bin” and “libnvvp” folder full path, and add into environment virables as new path.  
    e.g. C:\Program Files\NVIDIA GPU Computing Toolkit\CUDA\v11.2\bin  
    & C:\Program Files\NVIDIA GPU Computing Toolkit\CUDA\v11.2\libnvvp
- **Restart computer**
- **After restart, open Command Prompt “run as administrator”**
    
    ```python
    python -m pip install --upgrade pip
    ```
    
    ```python
    pip install tensorflow-gpu
    ```
    
    ```python
    pip3 install --upgrade tensorflow-gpu
    ```
    
- **Download Visual Studio Code**  
(https://code.visualstudio.com/download)  
- **Open VScode download extensions Python & Jupyter**
- **test code**
    
    ```python
    import tensorflow as tf
    print('tensorflow version', tf.__version)
    
    x = [[3.]]
    y = [[4.]]
    print('Result: {}'.format(tf.matmul(x,y)))
    ```
    
- **run with Python 3.10, should come up with**
    
    ```python
    tensorflow version 2.5.0
    Result: [[12.]]
    ```
