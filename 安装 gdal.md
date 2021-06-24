## 安装 gdal
conda search gdal
conda install -n 环境名称 gdal=版本号

## 升级conda
conda update -n base conda

conda install -c conda-forge gdal



## 步骤如下：
1.升级conda;

2.pip安装gdal 失败；

3.sudo apt-get install libgdal-dev 失败；

4.sudo aptitude install libgdal-dev 成功；

5.sudo apt-get install gdal-bin 成功；

6.conda  install -c conda-forge gdal

提示冲突，让系统自己处理

多试几次

最后

成功！

## 更新了mintpy环境的依赖项：
conda env update -f /home/melon/Mintpy/docs/conda_env.yml
