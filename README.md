# 小秘 · 发布通道

小秘 Android 客户端的更新清单和安装包。**源码不在这里**（在另一个私有仓库）。

这个仓库之所以公开，只有一个原因：手机上的「检查更新」要能**不带任何凭证**
拉到清单和 APK。这里没有密钥，也没有源码。

## update.json

```json
{
  "versionCode": 11,
  "versionName": "0.11",
  "url": "https://github.com/.../releases/download/v0.11/mishu-0.11.apk",
  "sha256": "<64 位小写>",
  "notes": "本版改了什么"
}
```

app 拿 `versionCode` 跟本地比大小，只有更大才提示更新；下载完**必须**
校验 `sha256`，对不上就丢弃不安装。地址必须是 https。

## 手动安装

从 [Releases](../../releases) 下最新的 APK。首次安装要允许"未知来源"。
后续版本签名相同，可以直接覆盖升级。
