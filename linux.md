anaconda版本Anaconda3-2021.11-Linux-x86_64.sh

上级目录

```
cd ..
```

英伟达; 查看cpu信息

```
nvidia-smi
top
```

列出文件

```
ls
```

激活pytorch虚拟环境

```
module load pytorch
source activate
conda activate xing  # 自建虚拟环境，支持cuda
```

torch gpu信息

```
import torch

print(torch.cuda.is_available() )# cuda是否可用
print(torch.cuda.device_count() )# gpu数量
print(torch.cuda.current_device())# 当前设备索引, 从0开始
print(torch.cuda.get_device_name(0))# 返回gpu名字
```

查看文件大小

```
du -hd0 :表示查询当前目录下总空间大小
du -hd1 :表示分别查询当前目录下的各目录的总空间大小
du -hd0 指定目录: 表示查询当前目录下指定目录总空间大小
```

移动文件

```
mv file filepath
```

系统内核

```
uname -a   # x86_64
```

本地安装库

```
pip install xxx.whl  # whl文件
cd to unzip filepath # tar.gz文件
python setup.py install
```

编辑文件

```
vi  vim
i      # 当前位置编辑
esc    # 退出编辑
：wq！ # 强制写入并推出
：q！  # 强制退出
https://blog.csdn.net/u012106306/article/details/94722875
https://www.cnblogs.com/mjoker0416/p/9869621.html
```

当前路径

```
pwd
```

安装错误，管理员身份进入命令行，cd到文件目录输入文件名安装

不挂起任务; 写入到某一文件中; 杀死任务

```
nohup [command] &
nohup [command] > filename.log 2>&1 &
kill -9 [pid]
ps -e -o stat,ppid,pid,cmd | egrep '^[Zz]'
fuser -v /dev/nvidia*  # 释放xmcy
```

删除除某一文件的其他文件

```
rm -v !("filename")
```

github,在某目录下打开git bash

```
git status                # 查看当前仓库状态
git add .                 # 代码保存到暂存区
git commit -m "备注内容"  # 提交更改
git push                  # 代码同步
git clone url             # 克隆到本地
```