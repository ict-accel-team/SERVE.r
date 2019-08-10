SERVE.r平台使用手册
=====
<changyisong@ict.ac.cn>
-----

## 使用步骤

1. 可使用PYNQ z1或z2系列板卡，并将板卡启动模式调整为SD卡启动  

2. 准备一张MicroSD卡，并使用分区工具将SD卡划分为boot区（FAT32）和 root区（Ext3）分区  

3. 将本仓库中bin目录下的BOOT.bin和RV_BOOT.bin两个文件拷入SD卡的boot区

4. 将Debian文件系统拷贝到SD卡的root分区（注意要使用特权模式）   
Debian文件系统的制作方式请参考：https://wiki.debian.org/RISC-V   

5. 将SD卡插入PYNQ板卡的SD卡槽   

6. 连接板卡的USB-UART接口到个人电脑的USB端口  
（注意：个人电脑请务必预先安装cp210x驱动和串口终端软件）   

7. 将开发板上电。板卡上电后，打开个人电脑上的串口终端软件，打开
对应的串口设备（COM），波特率设置为115200，无校验，无流控。  

8. 打开串口终端后，即可看到RISC-V Linux的启动过程

