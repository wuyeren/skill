# vibe-symlink-probe-repo

授权安全测试工件：验证 vibe `POST /skills/clone` 的 packDirectoryToZip
对符号链接的解引用行为（服务端任意文件读取）。

| 文件 | 指向 | 验证点 |
|------|------|--------|
| env | /proc/self/environ | vibe JVM 进程环境变量（凭证暴露面） |
| cmdline | /proc/self/cmdline | JVM 启动命令行 |
| cgroup | /proc/self/cgroup | 容器化信息 |
| passwd | /etc/passwd | 基础读取原语 |
| hosts | /etc/hosts | 网络信息 |
| os-release | /etc/os-release | 系统版本 |
| hostname-rel | ../../etc/hostname | 相对路径穿越（tempDir 之上） |
