# FishImagen EXE 下载

此仓库**只发布 Windows 二进制包，不包含源码、号池、个人配置或账号数据**。

## 安装

1. 下载 `ImageStudio_v0.1.1_binary.zip`，解压并保留完整的 `ImageStudio/` 文件夹。
2. 双击 `ImageStudio.exe`；它必须与 `_internal/` 放在同一目录，不能单独下载 EXE。
3. 配置与数据只写在用户本地的 `config.json` 和 `data/`，不会包含在此下载包中。

## 自动更新

`version.json` 是更新清单，包含版本号、ZIP 文件名、字节大小与 SHA-256。软件启动后及之后每小时检查一次；发现更高版本时在顶栏提示。点击下载后校验文件，再自动重启安装。安装器**只替换 EXE 与 `_internal/`**，保留本机 `config.json` 和 `data/`。

以后发布新版：先修改项目 `VERSION` 和 `backend/VERSION`，通过 BuildTool 重新打包，然后运行 `pack-release.ps1`，将生成的 ZIP 与 `version.json` **一起提交到本仓库**。必须保证清单的 SHA-256 与上传的 ZIP 一致。不要提交源码或本机数据库。
