# Pioneer
**沁恒CH32V307VCT6（RISC-V）核心板板卡Pioneer, 如有疑问请自行解决，不提供答疑（未经作者许可，请勿商用）**  
Copyright (c) 2024 Guangdong University of Technology.  
Author : Mingcong Wang  
Date : 2024.11.20  
![e9681bd7f2c93a74fa5b934ec3ba9e3](https://github.com/user-attachments/assets/fe6f3c39-c11e-47cc-8991-da3a9376561b)

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
<img width="311" alt="控制台输出" src="https://github.com/user-attachments/assets/17e1997e-c6b2-43dd-a205-8956a9025a96">

## 3.KeyShot工程
CH32V307VCT6.bip

## 4.3D模型
CH32V307.step

## 5.原理图
![CH32V307-01](https://github.com/user-attachments/assets/4e2edc87-fb2c-47d4-bbf4-0b2441d7b921)

## 6.3D渲染图

<img width="501" alt="9a2d31423b443c0dccbd2f5d3a3dc1b" src="https://github.com/user-attachments/assets/09e05796-4070-4ecd-b9cf-285e11856b88">

<img width="495" alt="718cc0fcc5220deaca71a6e41590d02" src="https://github.com/user-attachments/assets/f724baab-3b09-4897-8e64-bf8514b3f116">

## 7.CH32V307+WCHLink中文参考手册



