---
layout: post
title: Cornerstone ignore UserInterfaceState.xcuserstate
category : 痕迹
tagline: "ios"
tags : [xcode, svn, tutorial]
comments : false
---
{% include JB/setup %}

在控制台 _cd_ 到项目目录下
*svn -v status* 查看文件的状态(M):

M   33769    33757 xxx         XXX.xcworkspace/xcuserdata/XXX.xcuserdatad/UserInterfaceState.xcuserstate

	svn delete --keep-local --force xcuserdata/user.xcuserdatad/UserInterfaceState.xcuserstate

此时，Cornerstone会显示它的状态为"？",右键Ignore。解决了，世界清静了:]


**PS:**
added *.xcuserstate to the Global Ignores 
	(Cornerstone -> Preferences -> Subversion -> turn off Use default global ignores -> add "\*.xcuserstate")