# 使用jupyter notebook (Hyp3数据处理)出现如下报错：

```shell
 “ImportError: FloatProgress not found. Please update jupyter and ipywidgets. See https://ipywidgets.readthedocs.io/en/stable/user_install.html”
```

这是因为jupyter或者ipywidgets没安装或者没关联造成

# 解决办法：

1. 卸载jupyter：pip uninstall jupyter

2. 安装jupyter：pip install jupyter

3. 安装ipywidgets：pip install ipywidgets

4. 关联：jupyter nbextension enable --py widgetsnbextension
