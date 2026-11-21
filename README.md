# Soha Example Skill Pack

This declarative plugin demonstrates repository installation in a compatible Soha server. Its root `plugin.manifest.json` declares an AI skill pack. Enable the installation to see it under registered extensions, then disable it to remove that registration. The sample has no executable code or skill assets.

With the local CLI profile pointing to that server, review the version, commit and checksum shown before confirming:

```sh
soha plugin install --profile local --repository https://github.com/opensoha/soha-plugin-example-skill-pack --ref v0.1.1
```

To validate the root manifest and print its raw-byte SHA-256, use Node.js 22 or later:

```sh
npm ci --ignore-scripts
npm test
```

Publish a new plugin version for manifest changes so existing version tags and catalog snapshots stay reproducible.

## 中文

这是用于演示 Soha 仓库直装的声明式插件。根目录的 `plugin.manifest.json` 声明一个 AI 技能包。安装后手动启用，在已安装插件详情的「已注册扩展」中查看，停用后注册会消失。样例只有扩展声明。

上方命令使用已指向兼容自托管实例的 `local` profile。确认前请核对预览中的版本、固定提交和摘要。使用 Node.js 22 或以上版本运行 `npm ci --ignore-scripts` 和 `npm test`，可校验清单并输出其原始字节摘要。修改清单时发布新版本，以便复现已有版本和目录快照。

Licensed under [Apache-2.0](./LICENSE).
