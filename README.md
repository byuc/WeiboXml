# WeiboXml

> 使用RSS(XML格式)订阅喜欢的微博博主



## 介绍

部署URL：https://xxx.com/rss/{微博博主的uid}

RSS 格式输出一个微博博主最新的 15 条微博，可以使用 RSS 阅读器来获取及时推送，配合 [IFTTT](https://ifttt.com/) 还可以实现更多好玩的功能。

Demo：https://XXX.com/negative/{微博博主的uid}

<!-- 使用 [Text2Emotion](https://github.com/DIYgod/Text2Emotion) 实现，仅输出消极情绪的微博，用来监控博主的消极情绪。 -->

## 使用

使用 RSS 阅读器订阅：https://xxx.com/rss/{微博博主的uid}

## 获取微博UID
获取uid：进入博主的微博主页，控制台执行
```js
/uid=(\d+)/. exec(document.querySelector('.opt_box .btn_bed').getAttribute('action-data'))[1]
```

## Docker搭建

需要环境：Node.js

推荐使用 Docker
```
docker build .
docker run --name Weibo2RSS -p 1206:1206 -d [CONTAINER ID]
```
注意CONTAINER ID不是填写Node.js imagesID

## Copyright
原项目[Weibo2RSS](https://github.com/DIYgod/Weibo2RSS)已被原作者弃用，并入[RSSHub](https://github.com/DIYgod/RSSHub)进行维护  
原版权声明：MIT© [DIYgod](http://github.com/DIYgod)