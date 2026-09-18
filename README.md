### ✅ 第一步：Fork 本仓库

打开本项目页面 → 点击右上角 Fork 按钮（复制到你自己的 GitHub 账号下）

### ✅ 第二步：设置变量（多账号设置）

回到你的 GitHub 仓库页面 → 点上方 Settings → 左侧 Secrets and variables → Actions→ 点 New repository secret：
按下面格式填写

Name: 

```
ACCOUNTS
```
Secret:
```
aaa@qq.com:123456
bbb@qq.com:abcdef
ccc@qq.com:qwerty
```
一行一个账号。不要加空格。

### NTFY 消息推送（选填）

至少配置以下 Secret：

Name:
```
NTFY_TOPIC
```
Secret:
```
你的 NTFY 主题名称
```

如果使用自建 NTFY 服务，请配置：

Name:
```
NTFY_SERVER
```
Secret:
```
https://你的-ntfy-服务器地址
```

未配置 `NTFY_SERVER` 时，默认使用 `https://ntfy.sh`。

如果主题需要访问令牌，请配置：

Name:
```
NTFY_TOKEN
```
Secret:
```
你的 NTFY 访问令牌
```

未配置 `NTFY_TOPIC` 时，签到任务仍会正常执行，但会跳过消息推送。

### ✅ 第三步：测试运行

点击上方 Actions

首次 Fork 在 Actions 页面点击 Enable workflows 以启用自动任务。

选择 Auto Sign-in for BBS

点击右侧 Run workflow → 等待运行完成
