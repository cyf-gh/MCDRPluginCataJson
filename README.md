# MCDRPluginCataJson

* 页面：https://www.cyf-cloud.cn/#/util/mcdrPlg

## JSON 文件结构
如果你要上传插件，则先fork然后修改feed.json后PR。

feed.json的结构形如：
```
[
{
  "cat":"分类1",
  "plg":[
    {
      "name": "插件名1",
      "git":"https://github.com/who/plg.git",
      "desc": "插件描述"
    },
    {
      "name": "插件名2",
      "git":"https://github.com/who/plg2.git",
      "desc": "插件描述2"
    }
  ]
},{
  "cat":"分类2",
  "plg":[
    {
      "name": "插件名3",
      "git":"https://github.com/who/plg3.git",
      "desc": "插件描述3"
    }
  ]
}
]
```
如果你的插件的分类已存在，则在改分类的plg节点下直接填写：
```
    {
      "name": "插件名",
      "git":"https://github.com/who/plg.git",
      "desc": "插件描述"
    }
```
如果你的插件不属于任何分类，则需要添加一个分类：
```
{
...
  "cat":"分类",
  "plg":[
    {
      "name": "插件名",
      "git":"https://github.com/who/plg.git",
      "desc": "插件描述"
    }
  ]
...
}
```
PR前请保证json文件的正确性。
