# 企业微信群机器人 sdk 🤖 ![test](https://github.com/happysooner/workWechatRobot/workflows/test/badge.svg)

> 企业微信机器人发送消息 sdk,[官方文档](https://work.weixin.qq.com/api/doc/90000/90136/91770)

## 接口

> key 是指机器人接口的 queryString 中参数 key 的值

```
import "github.com/happysooner/workWechatRobot"

var robot = Robot{Key: "一个神秘的key"}

// 发送文本消息
_,_ = robot.SendText("文本发送测试！")

// 发送md消息
_,_ = robot.SendMarkdown("文本发送测试！")

// 发送图片
_,_ = robot.SendImage("图片base64","源图片的md5")

// 发送图文
ns := []*NewsItem{
		{
			Title:       "卡片消息标题",
			Description: "卡片消息描述",
			URL:         "https://happysooner.com",
			Picurl:      "http://res.mail.qq.com/node/ww/wwopenmng/images/independent/doc/test_pic_msg1.png",
		},
	}

_, _ := robot.SendNews(ns)
```
