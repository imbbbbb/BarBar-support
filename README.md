# BarBar 的更新源

这个分支只有一个作用：给 [BarBar](https://github.com/imbbbbb/BarBar-support)
的自动更新提供 `appcast.xml`。

- **更新源地址**：https://imbbbbb.github.io/BarBar-support/appcast.xml
- **安装包**：挂在本仓库的 [Releases](https://github.com/imbbbbb/BarBar-support/releases)

`appcast.xml` 不要手改。它由发版脚本 `Tools/appcast.sh` 生成，里面每个
`enclosure` 都带一段 EdDSA 签名 —— 手改之后签名对不上，所有用户的自动更新
会一起失败，而客户端只会安静地什么都不做。

文档和反馈入口在 `main` 分支。
