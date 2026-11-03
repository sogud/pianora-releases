# pianora-releases
琴昼 · Pianora 官方下载与版本更新。安装包、更新说明及第三方许可。

## 安装

适用于 Apple Silicon Mac。在「终端」里运行：

```sh
curl -fsSL https://raw.githubusercontent.com/sogud/pianora-releases/main/install.sh | sh
```

脚本会下载最新版本（包括测试版，安装包约 400 MB），校验 SHA-256，把 `Pianora.app` 装到「应用程序」（没有写入权限时装到 `~/Applications`）。用这种方式安装不会弹出 Gatekeeper 拦截。指定版本：`curl -fsSL … | VERSION=v0.3.0-beta.1 sh`；卸载：`curl -fsSL … | sh -s -- --uninstall`（不删练习记录和设置）。安装前可以先看看[脚本内容](install.sh)。

<details>
<summary>手动安装 / 提示「无法验证开发者」</summary>

琴昼 · Pianora 只做了本地临时签名，没有经过 Apple 公证，所以用浏览器下载后第一次打开会被拦截。

1. 在 [Releases](https://github.com/sogud/pianora-releases/releases) 下载 `Pianora-<版本>-mac-arm64.zip`，解压后把 `Pianora.app` 拖进「应用程序」。
2. 方法一：在终端运行
   ```sh
   xattr -dr com.apple.quarantine /Applications/Pianora.app
   ```
3. 方法二：先双击打开一次，然后进入 **系统设置 → 隐私与安全性**，在下方找到「已阻止打开 Pianora」，点 **仍要打开**，再输入密码确认。

</details>
