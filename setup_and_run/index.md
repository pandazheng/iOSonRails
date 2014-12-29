作为一个iOS开发，相信很多人和我一样将给自己的app快速的建立后端Server,把各种高负荷的计算工作都扔到后端，这样app的开发就可以重点放在提高用户体验上。而作为一个Ruby开发者，我们同样希望自己优雅的Ruby代码不仅仅作为Web app的后端，更希望自己也能够给自己的后端写iOS的app，没事在拥挤的地铁上无聊时候玩玩。所以我希望对自己的定义是“一个喜欢Ruby的iOS开发者”，我将会陆续的分享我使用Rails作为自己app后端的经验，每一次的分享都将是一个完整的项目，也就是你可以直接clone我放在github上面的项目，然后在自己的本地完美的跑起来，由浅入深。我想把这一系列称之为“iOS on Rails”

####需求
我们要做一个自己的新闻客户端。
####分析
这就是一个很典型的需要后端支持的app的场景，app不可能去代替后端去完成新闻的获取，信息的处理等工作，app的目的是为终端用户提供最优质的新闻阅读体验。
####实现
* Rails

有很多种方式去为iOS app搭建一个后端，但是也许Rails是最快的方式，Rails让我们可以在几分钟之内就可以搭建起一个干净的API server：backend-as-a-service. 显然我们app需要的resource是新闻（news），那么我们的REST API应该是这样子：