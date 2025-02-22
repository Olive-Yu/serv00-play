# serv00 上的一些应用，包括 argo+vmess/vmess+ws/hy2/socks5/mtproto/alist/哪吒探针/sun-panel/webssh 等, 自动化部署、批量保号、进程防杀、消息推送

## 前置工作

1. 你需要有一个 serv00 帐号
2. 首次运行，无需使用面板，选 1 安装 serv00-play, 它会自动重新登录，输入 ss 回车进入界面。(以后都是输入 ss 回车进入界面)

## 安装说明

```s
bash <(curl -Ls https://raw.githubusercontent.com/Olive-Yu/serv00-play/refs/heads/main/start.sh)
```

## 变量说明

| 变量名          | 示例   | 备注                                                                             |
| --------------- | ------ | -------------------------------------------------------------------------------- |
| HOSTS_JSON      | 见示例 | 可存放 n 个服务器信息 (必选)                                                     |
| TELEGRAM_TOKEN  | 略     | telegram 机器人的 token (发送 TG 消息必选)                                       |
| TELEGRAM_USERID | 略     | 待通知的 teltegram 用户 ID (发送 TG 消息必选)                                    |
| WXSENDKEY       | 略     | server 酱的 sendkey，用于接收微信消息 (发送微信消息必选)                         |
| SENDTYPE        | 1      | 选择推送方式，1.Telegram, 2.微信, 3.都有 (发送消息必选)                          |
| BUTTON_URL      | 略     | 设置 TG 推送消息中的按钮链接 (发送 TG 消息可选),支持#HOST，#USER，#PASS 等变量。 |
| AUTOUPDATE      | Y/N    | 设置是否自动更新服务器上的代码,设置在 variable 变量中，值为 Y/N(默认: Y)         |
| LOGININFO       | Y/N    | 在 variable 变量中设置(默认为 N)，Y:发送登录汇总消息 N:只在登录失败时发送        |
| TOKEN           | 123456 | 网页保活(keepalive)的密钥(必选)                                                  |


更新内容：
Nezha 探针更新到V1 版本，个人测试使用，使用青龙面板定时访问网页进行保活。
