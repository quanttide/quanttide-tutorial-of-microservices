# 配置中心

我们的Django应用的配置大概有一大半是重复的，使用几乎相同的中间件等等。

1. 使用共同的模板。目前我们有一个Django项目和应用模板。这个方案目前只能解决初始化项目的问题，一旦需要整体升级方案就又不方便了。
2. 使用网格的配置中心。如果我们把这部分重复配置拿出来到配置中心里，可以大大减少维护难度。

不过这里需要考虑和Dynaconf库的适配问题，比如说提供一个自定义loader方便库里接入。具体怎么做暂时还没有思路，不确定是下载以后缓存还是直接获取远端配置。
