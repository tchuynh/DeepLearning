




## dev ec2 large
```bash

ssh -i "~/Documents/test.pem" ec2-user@ec2-3-88-208-246.compute-1.amazonaws.com

=============================================================================
       __|  __|_  )
       _|  (     /   Deep Learning AMI GPU TensorFlow 2.10.0 (Amazon Linux 2) 
      ___|\___|___|
=============================================================================
TensorFlow 2.10.0 and utility libraries are installed in /usr/local/bin/python3.9.
To access them, use /usr/local/bin/python3.9.
NVIDIA driver version: 510.47.03
CUDA version: 11.2 
AWS Deep Learning AMI Homepage: https://aws.amazon.com/machine-learning/amis/
Release Notes: https://docs.aws.amazon.com/dlami/latest/devguide/appendix-ami-release-notes.html
Support: https://forums.aws.amazon.com/forum.jspa?forumID=263
For a fully managed experience, check out Amazon SageMaker at https://aws.amazon.com/sagemaker
Security scan reports for python packages are located at: /opt/aws/dlami/info/
=============================================================================


screen 

jupyter lab --ip=0.0.0.0 --port=8889


ssh -L 8889:127.0.0.1:8889 ec2-user@ec2-3-88-208-246.compute-1.amazonaws.com -i ~/Documents/test.pem


apt update all

mkdir -p ~/miniconda3
wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh -O ~/miniconda3/miniconda.sh
bash ~/miniconda3/miniconda.sh -b -u -p ~/miniconda3
rm -rf ~/miniconda3/miniconda.sh
~/miniconda3/bin/conda init bash
~/miniconda3/bin/conda init zsh


conda install jupyterlab jupyter numpy pandas tensorflow --yes
conda update tensorflow




````

```bash
2022-10-19 00:41:06.898099: I tensorflow/core/platform/cpu_feature_guard.cc:193] This TensorFlow binary is optimized with oneAPI Deep Neural Network Library (oneDNN) to use the following CPU instructions in performance-critical operations:  AVX2 AVX512F FMA
To enable them in other operations, rebuild TensorFlow with the appropriate compiler flags.
2022-10-19 00:41:37.273329: E tensorflow/stream_executor/cuda/cuda_blas.cc:2981] Unable to register cuBLAS factory: Attempting to register factory for plugin cuBLAS when one has already been registered
2022-10-19 00:42:14.934976: W tensorflow/stream_executor/platform/default/dso_loader.cc:64] Could not load dynamic library 'libnvinfer.so.7'; dlerror: libnvinfer.so.7: cannot open shared object file: No such file or directory; LD_LIBRARY_PATH: /opt/amazon/efa/lib64:/opt/amazon/openmpi/lib64:/usr/local/cuda/efa/lib:/usr/local/cuda/lib:/usr/local/cuda:/usr/local/cuda/lib64:/usr/local/cuda/extras/CUPTI/lib64:/usr/local/cuda/targets/x86_64-linux/lib:/usr/local/lib:/usr/lib:/lib:
2022-10-19 00:42:14.935172: W tensorflow/stream_executor/platform/default/dso_loader.cc:64] Could not load dynamic library 'libnvinfer_plugin.so.7'; dlerror: libnvinfer_plugin.so.7: cannot open shared object file: No such file or directory; LD_LIBRARY_PATH: /opt/amazon/efa/lib64:/opt/amazon/openmpi/lib64:/usr/local/cuda/efa/lib:/usr/local/cuda/lib:/usr/local/cuda:/usr/local/cuda/lib64:/usr/local/cuda/extras/CUPTI/lib64:/usr/local/cuda/targets/x86_64-linux/lib:/usr/local/lib:/usr/lib:/lib:
2022-10-19 00:42:14.935182: W tensorflow/compiler/tf2tensorrt/utils/py_utils.cc:38] TF-TRT Warning: Cannot dlopen some TensorRT libraries. If you would like to use Nvidia GPU with TensorRT, please make sure the missing libraries mentioned above are installed properly.
Found 20000 files belonging to 2 classes.
2022-10-19 00:42:44.399124: E tensorflow/stream_executor/cuda/cuda_driver.cc:265] failed call to cuInit: CUDA_ERROR_NO_DEVICE: no CUDA-capable device is detected
2022-10-19 00:42:44.399178: I tensorflow/stream_executor/cuda/cuda_diagnostics.cc:156] kernel driver does not appear to be running on this host (ip-172-31-95-77.ec2.internal): /proc/driver/nvidia/version does not exist
2022-10-19 00:42:44.642424: I tensorflow/core/platform/cpu_feature_guard.cc:193] This TensorFlow binary is optimized with oneAPI Deep Neural Network Library (oneDNN) to use the following CPU instructions in performance-critical operations:  AVX2 AVX512F FMA
To enable them in other operations, rebuild TensorFlow with the appropriate compiler flags.
```



## test ec2
```bash
 ssh -i "~/Documents/test.pem" ec2-user@ec2-54-221-17-79.compute-1.amazonaws.com

ssh -L 8888:127.0.0.1:8888 ec2-user@ec2-54-221-17-79.compute-1.amazonaws.com -i ~/Documents/test.pem


jupyter lab --ip=0.0.0.0 --port=8889
````







```bash



mkdir -p ~/miniconda3
wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh -O ~/miniconda3/miniconda.sh
bash ~/miniconda3/miniconda.sh -b -u -p ~/miniconda3
rm -rf ~/miniconda3/miniconda.sh
~/miniconda3/bin/conda init bash
~/miniconda3/bin/conda init zsh


conda install jupyterlab jupyter numpy pandas
conda install tensorflow --yes
conda update tensorflow



ssh -L 8888:127.0.0.1:8888 root@ec2-18-205-188-57.compute-1.amazonaws.com -i ~/Documents/test.pem


alias tunnel=“ssh -L 8888:127.0.0.1:8888 root@ec2-18-205-188-57.compute-1.amazonaws.com -i ~/Documents/test.pem”


ssh -L 8888:127.0.0.1:8888 root@ec2-18-205-188-57.compute-1.amazonaws.com -i ~/Documents/test.pem


ssh -L 8888:127.0.0.1:8888 ec2-user@ec2-18-205-188-57.compute-1.amazonaws.com -i ~/Documents/test.pem




http://ip-172-31-95-77.ec2.internal:8888/lab?token=0da1f1d6ad76bfeec5f19b1c2cbaedf6c084274d3b0af530

jupyter lab --allow-root --ip 0.0.0.0 



lsof -i -P | grep LISTEN | grep :$PORT

netstat -anvp tcp | awk 'NR<3 || /LISTEN/'


sudo lsof -PiTCP -sTCP:LISTEN

````