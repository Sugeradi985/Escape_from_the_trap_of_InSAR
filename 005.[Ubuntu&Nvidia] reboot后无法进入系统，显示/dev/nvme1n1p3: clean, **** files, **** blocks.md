该死的工作站 开机（或重启）时卡在登录界面，内核打印消息如下：

``` shell
/dev/nvme1n1p3: clean, **** files, **** blocks
[   5.004707] nvidia-gpu 0000:05:00.3: i2c timeout error e0000000
[   5.004734] ucsi_ccg 0-0008: i2c_transfer failed -110
[   5.004772] ucsi_ccg 0-0008: ucsi_ccg_init failed - -110
```

## 解决方案：

1. 在grub启动界面，选择第二项"ubuntu高级设置"，回车
![image](https://user-images.githubusercontent.com/83938492/129685158-cadf75e3-0c6b-4867-bbd9-c68e5500398a.png)

2. 选择第二项"recovery mode"，按一下键盘上的"e"键，进入编辑模式：
![image](https://user-images.githubusercontent.com/83938492/129685206-f6f5797e-3092-4af7-a14c-a4c235504e43.png)

3. 将"ro recovery nomodestset"，修改为"rw single init=/bin/bash"并删除该行后面内容
![image](https://user-images.githubusercontent.com/83938492/129685226-2e895279-944b-4f7e-b74a-f66f6d319383.png)

4. 按下ctrl+x运行配置进入单用户root模式

5. 输入命令行:

```shell
sudo vim /etc/modprobe.d/blacklist_i2c-nvidia-gpu.conf 
```

6. 在文件中添加以下内容后保存并退出：

```shell
blacklist i2c_nvidia_gpu
```

重新启动,即可进入系统.
