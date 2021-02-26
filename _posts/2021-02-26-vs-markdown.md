---
layout: post
title: VS code中markdown默认代码片段(snnipt)配置
subtitle: 
date: 2021-02-26
author: LeeSongt
catalog: true
published: false
tags: 
    - system
---

## 如何在VS code中支持markdown默认代码片段的配置

* 打开【vs code】>>【File】>>【Preferences】>>【User Snippets】>>【markdown.json】

* 编辑默认代码片段

```json
{
	"Print to console": {
		"prefix": "post",
		"body": [
			"---",
			"layout: post",
			"title: $0",
			"subtitle: ",
			"date: $CURRENT_YEAR-$CURRENT_MONTH-$CURRENT_DATE",
			"author: LeeSongt",
			"catalog: true",
			"tags: ",
			"    - default",
			"---"
		]
	}
}
```

* 打开【settings.json】,添加如下代码

```
  "[markdown]": {
    "editor.quickSuggestions": true
  }
```

* 重启`VS Code`使配置生效。