# Enjoyable 中文说明

[English README](README.md)

Enjoyable 是一个 macOS 应用，可以把手柄、摇杆等控制器输入映射成键盘和鼠标操作。

如果你玩的游戏只支持键盘和鼠标，但你想改用手柄，Enjoyable 就是做这件事的。

本仓库维护自上游项目：
[matthewyang204/Enjoyable](https://github.com/matthewyang204/Enjoyable)

## 功能

- 将手柄按键映射到键盘按键
- 将摇杆映射到鼠标移动或滚轮
- 支持多套映射并可动态切换
- 支持导入和导出映射预设

## 使用方式

启动后，先按一下手柄上的按键或摇杆方向，再按下你想映射到的键盘按键即可。

更多说明可以在应用内通过 `⌘?` 打开帮助。

## 系统要求

- macOS 11 或更高版本
- 一个或多个兼容 HID 的输入设备（USB 或蓝牙手柄都可以）

## 构建与运行

日常开发建议直接使用根目录的 `Makefile`：

```bash
make build
make run
```

常用命令：

```bash
make open
make install
make release
make install-release
make clean
```

如果 `xcodebuild` 提示你还没有接受 Xcode 许可协议，先执行：

```bash
sudo xcodebuild -license
```

## 安装到自己的电脑

### 方式 1：命令行安装

构建并安装到当前用户的 `~/Applications`：

```bash
make install
```

如果你想安装 Release 版本：

```bash
make install-release
```

安装完成后，你可以直接打开：

```bash
open ~/Applications/Enjoyable.app
```

### 方式 2：手动安装

先构建：

```bash
make build
```

然后把下面这个 `.app` 拖到 `Applications` 或 `~/Applications`：

```text
build/Build/Products/Debug/Enjoyable.app
```

## 无法打开应用

如果 macOS 提示应用来自“未识别的开发者”，可以在管理员终端中执行：

```bash
sudo spctl --master-disable
```

## 版权与许可

原始版权归原项目作者所有，许可协议与英文版 README 保持一致。

## 致谢

- [erpapa's Enjoyable 1.3](https://github.com/erpapa/Enjoyable-1.3)
