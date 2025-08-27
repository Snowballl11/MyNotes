# WSL 2 常用命令参考

**作者：** Your Name
**日期：** 2025年5月23日

WSL 2 (Windows Subsystem for Linux 2) 提供了丰富的命令行工具，用于管理和操作您的 Linux 发行版。以下是常用的命令及其功能。

## WSL 2 基本操作与管理命令

### 查询与状态

```bash
wsl --list # (或 wsl -l)
# 查看所有已安装的 WSL 发行版名称。

wsl --list --verbose # (或 wsl -l -v)
# 列出所有已安装的 WSL 发行版，显示其状态 (例如：Running, Stopped) 和版本 (1 或 2)。

wsl --status
# 显示默认 WSL 发行版、默认版本和内核版本等信息。
```
**说明：** 查询 WSL 状态

### 启动与停止

```bash
wsl
# 启动默认的 WSL 发行版。

wsl -d <发行版名称>
# 启动指定的 WSL 发行版。
# 例如：wsl -d Ubuntu

wsl --shutdown
# 立即关闭所有正在运行的 WSL 发行版。

wsl --terminate <发行版名称> # (或 wsl -t <发行版名称>)
# 终止指定的 WSL 发行版。
# 例如：wsl --terminate Ubuntu
```
**说明：** 启动与停止 WSL 发行版

### 版本管理

```bash
wsl --set-default-version <版本号>
# 设置默认的 WSL 版本，通常推荐设置为 2。
# 例如：wsl --set-default-version 2

wsl --set-version <发行版名称> <版本号>
# 将指定的发行版转换为 WSL 1 或 WSL 2。
# 例如：wsl --set-version Ubuntu 2
```
**说明：** WSL 版本管理

### 安装与卸载

```bash
wsl --install
# 自动安装默认的 Ubuntu 发行版和 WSL 所需组件。

wsl --install -d <发行版名称>
# 安装指定的 WSL 发行版。
# 例如：wsl --install -d Debian

wsl --unregister <发行版名称>
# 卸载并删除指定的 WSL 发行版的所有数据。此操作不可逆，请谨慎使用。
# 例如：wsl --unregister Ubuntu
```
**说明：** 安装与卸载 WSL 发行版

### 导入与导出

```bash
wsl --export <发行版名称> <文件名>
# 将指定的 WSL 发行版导出为 .tar 文件，可用于备份或迁移。
# 例如：wsl --export Ubuntu D:\WSL_Backup\ubuntu_backup.tar
```
**说明：** 导入与导出 WSL 发行版

### 更新与配置

```bash
wsl --update
# 更新 WSL 内核和 WSL 功能。

wsl --update --rollback
# 回滚到上一个 WSL 版本。

wsl --upgrade
# （仅适用于通过 Microsoft Store 安装的发行版）升级发行版。
```
**说明：** 更新与配置 WSL

### 网络相关 (WSL 2 特有)

由于 WSL 2 运行在轻量级虚拟机中，其网络行为与 WSL 1 不同。

```bash
# 在 WSL 2 终端中获取 IP 地址：
ip a | grep eth0 | grep inet | awk '{print $2}' | cut -d/ -f1
# 获取 WSL 2 实例的 IPv4 地址，用于从 Windows 访问 WSL 2 服务。

# 在 Windows PowerShell (管理员) 中设置端口转发：
netsh interface portproxy add v4tov4 listenport=<Windows 端口> listenaddress=0.0.0.0 connectport=<WSL2 端口> connectaddress=<WSL2 IP 地址>
# 将 Windows 上的指定端口流量转发到 WSL 2 内部。
# 例如：netsh interface portproxy add v4tov4 listenport=80 listenaddress=0.0.0.0 connectport=8000 connectaddress=172.18.1.5

netsh interface portproxy delete v4tov4 listenport=<Windows 端口> listenaddress=0.0.0.0
# 删除指定的端口转发规则。
```
**说明：** WSL 2 网络相关

请注意，WSL 命令行工具持续更新，建议查阅 Microsoft 官方文档以获取最新信息。