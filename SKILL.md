---
name: symlink-read-probe
description: >
  [安全测试探针] 用于验证 vibe cloneSkillRepo 打包符号链接时的服务端文件读取问题。
  仅用于授权安全测试，请勿安装到生产项目。
---

# Symlink Read Probe（安全测试探针）

本技能是 vibe 平台安全审计的测试工件。仓库内的符号链接会在服务端
clone + packDirectoryToZip 阶段被解引用，用于验证服务端任意文件读取。
对应文件说明见 README.md。
