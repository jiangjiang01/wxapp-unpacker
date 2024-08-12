# 说明

- fork 自项目 https://gitee.com/ksd/wxappUnpacker
- 代码大致一样，仅修复了一处运行报错

# 安装

```
npm install
```

# 分包功能

当检测到 wxapkg 为子包时, 添加-s 参数指定主包源码路径即可自动将子包的 wxss,wxml,js 解析到主包的对应位置下. 完整流程大致如下:

1. 获取主包和若干子包
2. 解包主包 `./bingo.sh testpkg/master-xxx.wxapkg`
3. 解包子包 `./bingo.sh testpkg/sub-1-xxx.wxapkg -s=../master-xxx`

TIP

> -s 参数可为相对路径或绝对路径, 推荐使用绝对路径, 因为相对路径的起点不是当前目录 而是子包解包后的目录

# mac 下小程序源码包地址为

```
/Users/xxx/Library/Containers/com.tencent.xinWeChat/Data/.wxapplet/packages/xxxxxxxx/xx
```

目录中找到一个**APP.wxapkg**， 这是未加密的包，可以直接复现到该项目目录下执行

# window 下方法

直接下载 [`wxapkg.zip`](https://github.com/jiangjiang01/wxapp-unpacker/releases/tag/0.0.1)，然后使用命令行工具进入到该工具目录，执行 `wxapkg.exe scan`，工具会自动扫描，选择要处理的小程序即可。
参考：[https://github.com/wux1an/wxapkg](https://github.com/wux1an/wxapkg)
