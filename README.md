# Activation Script

[![Version][package-version-src]][package-version-href]
[![License][license-src]][license-href]

## Features

-   [x] Activate the application with MITM
-   [ ] ...What else? [Create a new issue](https://github.com/wibus-wee/activation-script/issues/new?assignees=&labels=enhancement&projects=&template=feature_request.yml)

###### [Our Roadmap](https://github.com/wibus-wee/activation-script/issues/15)

## Modules

目前支持的激活模块有：

-   [x] LemonSqueezy <sup>***`📦 Stable`***</sup>
-   [x] Paddle <sup>***`📦 Stable`***</sup>
-   [x] Gumroad <sup>***`📦 Stable`***</sup>
-   [x] App Store Restore Purchase <sup>***`🪄 Beta`***</sup>
-   [x] Shottr <sup>***`🪄 Beta`***</sup>
    -   [x] Basic Tier
    -   [ ] Friends Club
-   [x] Raycast Pro Plan <sup>***`🌊 Partially supported`***</sup>

###### [模块特殊说明](#特殊说明)

## 安装

前往 Surge 的 `Module` 配置页面，添加外部模块链接:

```text
https://github.com/wibus-wee/activation-script/raw/gh-pages/activator.sgmodule
```

或者你希望自行修改配置文件与脚本，你可以使用如下指令：

```bash
pnpm i
pnpm build:core # Build core(activator.js)

# CLI (When you want to use local module)
pnpm start:generator gen # Generate config
pnpm start:generator inject # Build activator.js and move to directory
pnpm start:generator patch # Patch Surge config file (Beta)
```

###### [项目结构](#项目结构)

## 特殊说明

### Paddle

-   [x] AlDente Pro
-   [x] iStatistica Pro
-   [x] One Switch
-   [x] Charliemonroe
    -   [x] Downie 4
    -   [x] Permute 3
-   [x] Sensei
-   [x] Rectangle Pro
-   [x] MenubarX
-   [x] MarginNote 3
-   [x] MWeb Pro

Paddle 是一个软件许可证管理服务。你可以使用以下指令查找使用了本机使用了 `Paddle.framework` 的应用程序：

```shell
find /Applications -name "Paddle.framework" -type d -exec sh -c 'echo "应用程序 {} 使用了 Paddle.framework"' \;
```

一般来说，它们都可以被正常激活。同时，也欢迎提交你发现的使用了 Paddle 的应用程序，我会将它们添加到列表中。

或许你需要许可证来触发激活程序，你可以使用以下激活码（fake）：

> 尤其针对 `com.charliemonroe` 的程序做了许可证格式的处理，因此你可以使用以下激活码来激活它们。

```
D7BC2F5F-E9BC2E9E-B4DA2D3C-E7FF3E9F-D3FA6C7F
A7DF3E8C-C2FD6B6E-E2EA2F6E-E7AD1E2F-B6DD8F2A
D6AE1F1C-E8BE9B3C-E3EC1D5B-B5BB8D4D-C1DC3C3D
F3BF4F2E-D7FE1B5B-E8BF7B6B-D7DA8A7A-F5FC7A4B
F2FC1F4B-F8FF7F8D-D9EE6E7A-D4FA9F2E-D1FA2A9A
B2AE7F7A-D5EE5C5F-F6CC6C6D-D4FF4C1E-C5DF6C9F
B6AA1C9B-E3FC7B8D-F8AE5F4E-A2CC6F9A-F5BE5E6B
D9BA5F4E-B8CA4E4D-B9AC7A1C-D2DA2A1D-E7BF9C2F
D1BC8C4B-E8EE7E4C-E1BD9A6B-A5EF3C3B-D7ED5E4B
C2BF5D3B-F4AC9F5F-A8EB4B9E-B8AA5E8D-E2CC5C8D
```

###### [Alogrithm](./packages/modules/paddle/alogrithm/gen.ts)

### App Store Restore Purchase

> [!WARNING]
> 由于 Apple 的限制，这个功能只能用于仍使用[旧式 verifyReceipt 验证（文档中已被弃用）](https://developer.apple.com/documentation/appstorereceipts/verifyreceipt)的应用。如果你的应用使用了新的验证方法，那么这个功能将无法正常工作。

欢迎提交你发现的使用了旧式验证的应用程序，我会将它们添加到列表中。

-   [x] iShot Pro

### LemonSqueezy

-   [x] Screen Studio

以下许可证可以用于激活 Screen Studio，但是其他应用程序暂时未能确定（因为找不到其他使用 LemonSqueezy 的应用程序）

```
401934ec-0a54-433c-a299-2a363501d4be
d06ad32e-00c2-43fb-a5a7-9bb44b094831
0c903cdd-9ee1-4935-8ad3-88de0ecef496
295aab81-b87e-437c-868a-1f0877216cae
4dc5cab3-03e0-41ab-827d-90dbe9e076f6
7a777528-c9b8-4db5-a986-0bd8d4312afd
d3ce015b-2093-42f5-a049-670edae6e7b4
f6e63b4e-91d4-4eb4-8dd0-dcb20933495e
f899ec8c-020b-4f8a-a09d-22a978b716a5
62c3bf31-428b-4bea-a31f-9a14f0a1a63c
```

###### [Alogrithm](./packages/modules/lemon-squeezy/alogrithm/screen-studio.ts)

### Gumroad

> Thanks to @QiuchenlyOpenSource & @Qiuchenly.

-   [x] MediaMate
-   [x] ...more

理论上，以下的激活码可以用于所有使用 Gumroad 的应用程序。

```
MNBVCXZLK-QWERTYUIO-ASDFHJKLZ-XCVBN
85DB562A-C11D4B06-A2335A6B-8C079166
ZTVKHMKYQ-JKDOSLFZU-UIXXTKLBA-HVNEZ
55277020-CAZNWFKK-97392017-MROIOCVV
WKMCDMKQS-RKLZHNWTW-OBLLJBZAX-VCEKT
94389301-ICWINLVW-35507779-OXCCQXLN
IXNIVXJUC-ZODUBIVHS-XNRCXLQVM-FVDHC
43378717-DHAMJHWK-86941225-DTMNMZRE
ZCJJBTBBT-XXTCCSCZT-XMVQQXQXL-ZVOZI
88079719-BONJCJQC-43235799-SODXFXIZ
IFZONWUNB-OWLYVQKQB-YFNIKSXBS-MCLRA
41389661-TLSYJYTE-32625842-BLCVBKVK
```

###### [Alogrithm](./packages/modules/gumroad/alogrithm/index.ts)

### Raycast Pro Plan

> Thanks to @zhuozhiyongde.

为了可以正常使用 Raycast Pro Plan，你可能需要在 `Surge -> HTTP -> 捕获 -> 捕获 MITM 覆写` 中修改 MITM 主机名，将最后一行 `*` 取消勾选。

如果后续你需要使用 Surge Dashboard 并正常使用原本的流量捕获功能，您需要重新勾选 `*`

> [!WARNING]
> 由于 Surge 限制，在 Surge 内的 runtime 做脚本无法实现 SSE，这对体验有很大很大的影响，以及还有一些实现上的问题，因此我打算不做内置的 AI 支持了

如果想使用 AI 功能，请参照以下项目搭建自己的后端服务进行体验： **（它们都是不一样的！）**

-   [wibus-wee/raycast-unblock](https://github.com/wibus-wee/raycast-unblock)
-   [zhuozhiyongde/Unlocking-Raycast-With-Surge](https://github.com/zhuozhiyongde/Unlocking-Raycast-With-Surge)
-   [yufeikang/raycast_api_proxy](https://github.com/yufeikang/raycast_api_proxy)

目前，Activation Script 仅会将 AI 部分的请求转发到你的后端服务。

> [!NOTE]
> 此部分是因为暂时无法对模块进行配置而导致的问题，在完成 Dashboard 功能后，你可以自行配置模块的启动与关闭，而无需修改代码。

<details>
  <summary>如果你需要把 translations 功能也转发给后端服务：</summary>

```diff
{
    base: 'translations',
-    func: raycastTranslate,
+    func: unblockRequest,
},
```

对于其他的 Route 你需要转发给后端服务，你也可以这么做。

</details>

另外，你可能还需要前往 [./packages/modules/raycast/universal.ts](./packages/modules/raycast/universal.ts) 或已构建的脚本中，修改替换的 `url` 为你自己的后端服务地址。

```diff
return Done({
    url: $request.url.replace(
        'https://backend.raycast.com',
-        'http://127.0.0.1:3000',
+        'https://your-backend-service.com',
    ),
    headers: $request.headers,
    body: $request.body,
})
```

> [!WARNING]
> 不要让 Surge 既代理 Raycast 的请求，又代理你的后端服务的请求，这会导致无法正常使用。
>
> 除非...除非你给 headers 加点[料](./src/modules/index.ts#L70)，让你的后端服务可以正常工作. (同时建议后端服务关闭 SSL 检查 `NODE_TLS_REJECT_UNAUTHORIZED=0`)

## 项目结构

```text
.
├── .github
│   └── workflows
├── .vscode
├── packages
│   ├── core
│   ├── modules
│   ├── generator
│   └── shared
└── ...others
```

- `core`: 核心模块，负责启动与运行时的匹配和运行逻辑
- `modules`: 模块集合，负责修改请求与响应
- `generator`: 生成器，负责生成配置文件与脚本
- `shared`: 共享模块，提供一些共享的工具（例如：储存、解析、类型支持）

## Credits

-   [Surge](https://nssurge.com/)
-   [QiuChenlyOpenSource/InjectLib](https://github.com/QiuChenlyOpenSource/InjectLib)
-   ~~[sooxt98/spotify-crack-chrome-app](https://github.com/sooxt98/spotify-crack-chrome-app)~~
-   [yufeikang/raycast_api_proxy](https://github.com/yufeikang/raycast_api_proxy)
-   ~~[sfc9982/typoraActivator](https://github.com/sfc9982/typoraActivator)~~

## License

This project is licensed under the AGPLv3 License. See the [LICENSE](LICENSE) file for details.

## Author

Activation Script © Wibus, Released under AGPLv3. Created on Sep 9, 2023

> [Personal Website](http://wibus.ren/) · [Blog](https://blog.wibus.ren/) · GitHub [@wibus-wee](https://github.com/wibus-wee/) · Telegram [@wibus✪](https://t.me/wibus_wee)

<!-- Badges -->

[package-version-src]: https://img.shields.io/github/package-json/v/wibus-wee/activation-script?style=flat&colorA=080f12&colorB=1fa669
[package-version-href]: https://github.com/wibus-wee/activation-script
[license-src]: https://img.shields.io/github/license/wibus-wee/activation-script.svg?style=flat&colorA=080f12&colorB=1fa669
[license-href]: https://github.com/wibus-wee/activation-script/blob/main/LICENSE
