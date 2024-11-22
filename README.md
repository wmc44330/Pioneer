# Pioneer
**沁恒CH32V307VCT6（RISC-V）核心板板卡Pioneer, 如有疑问请自行解决，不提供答疑（未经作者许可，请勿商用）**  
Copyright (c) 2024 Guangdong University of Technology.  
Author : Mingcong Wang  
Date : 2024.11.20  
![e9681bd7f2c93a74fa5b934ec3ba9e3](https://github.com/user-attachments/assets/7619b895-2301-4b42-be58-1e02d63afc21)


## 1.AD工程

Pionner-V1.1文件夹为Gerber文件，发给打板商既可  

如果需要制作钢网，也可以发这个文件夹（主要需要.GBP和.GTP）  

贴片的话暂时没用过，经费有限，手工焊接  

【板卡基本信息】：  
主控：CH32V307VCT6  
主频：144MHz  
RAM ：64K  
片上FLASH：256K  
硬件内核：青稞V4F (RISC-V)  
尺寸：5cm * 3.7cm  
外设资源：PWM-LED、BOOT按键、WK_UP按键、FSMC接口LCD、W25Q256、AT24C256、XPT2046电阻触摸芯片、WCH-Link(自带串口)、USB-OTG-FS、SWD下载口  


PCB层数：2层，为了节省成本，但是LCD屏幕的背光驱动电流比较大，两层在FPC接口的左侧电阻会发热，建议改四层  
备注：除了PE4、PE5、PE6引脚未引出，其余引脚全部引出，板卡集成WCH-Link，无需下载器（但是需要向板载WCH-Link烧写固件，请查看7.CH32V307+WCHLink中文参考手册），直接连Type-C线即可下载  

LCD屏幕大致20块左右，LCD屏幕链接：https://item.taobao.com/item.htm?id=682140966071  

板卡成本大致20块左右，加屏幕的话40块左右~  

芯片资料请自行到沁恒微电子官网（https://www.wch.cn/）下载  

--------------------------  
###有空的话再设计底板了###  

## 2.程序源码
驱动测试程序，没有过多使用RT Thread的内核对象，WK_UP按键代码需要小改
请自行搭建MounRiver Studio开发环境
程序控制台输出：
<img width="311" alt="控制台输出" src="https://github.com/user-attachments/assets/d9f272cf-1694-4d21-b7e3-894690af0130">


## 3.KeyShot工程
CH32V307VCT6.bip  
<img width="1279" alt="1c013af30e5a413c1df6d88d4c0f0c8" src="https://github.com/user-attachments/assets/f0e79c68-03d4-41a6-9495-6a22b60449d0">


## 4.3D模型
CH32V307.step  
<img width="1280" alt="3D模型" src="https://github.com/user-attachments/assets/7c7943c9-e4f3-4c5d-a9e4-49c9f9e07215">


## 5.原理图
![CH32V307-01](https://github.com/user-attachments/assets/70185e0d-9676-476e-a6d6-79e0f750a236)

## 6.3D渲染图
<img width="501" alt="9a2d31423b443c0dccbd2f5d3a3dc1b" src="https://github.com/user-attachments/assets/54fd4415-65c2-4dd3-b3ec-1db79e21d315">  
<img width="495" alt="718cc0fcc5220deaca71a6e41590d02" src="https://github.com/user-attachments/assets/f8f9e473-e592-43ba-88c0-79785f8dc467">



## 7.CH32V307+WCHLink中文参考手册



