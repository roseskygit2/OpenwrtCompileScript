# OpenwrtCompileScript

![CompileScript](doc/CompileScript.PNG) 
## 序言

用于辅助Openwrt编译，但不会帮你完成整个编译过程，需要一点Openwrt编译基础

降低编译难度，减少重复的步骤，但不利于学习，此脚本适用于有点openwrt编译的基础的最佳，完全没有编译基础的请去补充相关知识

 想学点东西请走这里： https://www.right.com.cn/forum/thread-324501-1-1.html

 此脚本并不是无脑脚本，这个脚本对新手是无脑的但要点基础，起码你要会选择机型与插件，有点基础的可以说是辅助，加快你的编译速度，写这个脚本的初衷就是编译的过程重复太多，所以写了脚本

> ### 感谢 @学渣 @sjz 等的帮助

## 支持系统

The script is made to work on these OS :

- Ubuntu 16.4
- Ubuntu 18.4 （首选，脚本基于此版本编写测试）
- win10子系统（ubuntu 18.04 LTS）
- Github Gitpod云编译(参考：https://www.right.com.cn/forum/thread-1573038-1-1.html)
- Deepin 15.11桌面版（群友测试ok）

## Usage 使用方法

1、使用git克隆下载脚本并赋予执行权限

```bash
git clone https://github.com/openwrtcompileshell/OpenwrtCompileScript.git && chmod +x OpenwrtCompileScript/openwrt.sh

```

2、进入脚本目录并执行

```bash
cd OpenwrtCompileScript && bash openwrt.sh
```

**注意**:执行脚本后会自动添加系统变量，第二次可使用如下命令运行脚本。

`bash $openwrt`

### 脚本详细使用方法

https://www.right.com.cn/forum/thread-345378-1-1.html

交流技术适当吹水群：667491026   （**拒绝大爷公子伸手党**)

## 版本修改记录

### ++2.8版本

1. 更新dl下载代码，
2. 补全if判断代码
3. 修复之前代码不完整
4. 新增变量openwrt_shfile
5. 调整代码的阅读顺序，方便阅读调整
6. 环境依赖加入判断，防止报错
7. openwrt加入lean插件功能
8. 颜色调整，方便阅读
9.  新增功能按键 更新lean仓库
10. 编写OpenwrtCompileScript使用说明.pdf
11. 将二次编译与源码更新模块合并，并加入显示远端仓库的最近三条更新内容模块
12. 加入比较源码参数
13. 取消官方源码强制https
14. 合并左右的部分脚本代码
15. 删除dl国内服务器下载功能选项
16. 增加software_Setting_Public模块

### ++2.7版本

1. 修改脚本名字为《openwrt.sh》不再以版本命名，以后执行脚本bash openwrt.sh即可
2. 加入if判断是否源码下载成功
3. Dl服务器下载增加一个参数，解决证书不信任问题
4. 增加脚本描述文本
5. 文件夹创建提前
6. 加入时间计算让自己更加直观看到编译耗时
7. 增加多线程编译可以自己决定以多少线程进行编译
8. 增加脚本自检程序
9. 新增选项 9.更新脚本
10. 优化一下代码
11. 增加一个ls函数模块
12. 适配win10子系统（ubuntu 18.04 LTS）
13. 删除无用的5.选项替换DNS

### ++2.6版本

1. 支持不在home底下也能正常运行，因为服了一下小白老是报错
2. 只需要执行脚本就可以操作你任意的openwrt文件夹
3. 新增国内DL服务器（感谢LGA1150）
4. 新增选择( 6.其他选项)，可以单独使用个别模块，如：支持单独只搭建编译环境，而不进行编译
5. 创建文件时加入判断，防止覆盖之前的目录
6. 删除之前的个别文件，脚本执行目录随意没有要求了，但Home目录底下的Openwrt目录禁止改名移动

### ++2.5版本

1. 简化之前目录
2. 代码的重写
3. 一个目录方便管理
4. 加入Lean_R9_source and Openwrt17.01_source

### ++2.4版本

1. 增加config文件保存与调用（家里机型较多的可以更省事），此建议由 @兔巴哥提供

### ++2.3版本

1. 合并功能按键并增加第5.HOST选项
