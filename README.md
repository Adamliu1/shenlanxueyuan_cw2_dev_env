# 快速开始

首先需要让英伟达可以使用docker，详见
```
https://docs.nvidia.com/datacenter/cloud-native/container-toolkit/latest/install-guide.html
```

clone该repo
```
git clone --recursive https://github.com/Adamliu1/shenlanxueyuan_cw2_dev_env.git
```

# 进入docker
```
cd docker/
```
因为需要用x11 GUI穿透，需要记得
```
xhost +
```

接着通过docker compose开启
```
docker compose -f docker-compose_gpu.yml up --build -d
```

通过vscode attch进去,然后使用conda/mamba激活环境
```
bash
mamba activate rl-ga
```

然后跟着，使用具体的训练代码
```
https://github.com/unitreerobotics/unitree_rl_gym/blob/757b05158058a2a8005810c2bb2e1e8667cf3f17/README_zh.md
```
### WSL用户参考
微软官方wsl的文档来实现docker在wsl内的gpu加速（通过修改docker-compose文件）
```
https://github.com/microsoft/wslg/blob/main/samples/container/Containers.md
```
