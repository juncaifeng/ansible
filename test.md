---
date: 2022-05-17 17:46:29
layout: post
---

[toc]
# 123
# 123
## 2
```
dssdadsad
```

  

**创建一个Pillar**

pillar在Salt中已经是默认运行的。minion中的pillars可以通过以下的命令来查看：

  

```javascript
salt "*" pillar.items
```

  
注意，在0.16.2之前的版本中，这个函数的名字是pillar.data。为了与以前版本兼容，这个函数名仍然是可用的。

  

默认情况下，master配置文件中的内容是被载入到每个minion的pillar中的。这使得master的配置文件可以作为所有minions的全局配置。

  

pillar和state tree的建立方式相似，由sls文件组成，并有一个top文件，这和state tree类似。pillar默认的路径是：/srv/pillar。

  

注意，pillar的位置可以通过master配置见中的pillar\_roots配置项来自定义