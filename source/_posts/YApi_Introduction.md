---
title: YApi简介
date: 2019-09-28
catalog: true
tags:
- YApi
- 开发工具
---
## YApi是什么？

​		YApi是去哪儿网大前端团队开发的一个接口管理平台，汲取了Rap、Nei、Easy-Mock等产品的设计灵感，同时提供了类postman、restlet等工具的调试能力，打通了前后端分离开发模式下的接口开发流程，解决了协作上的痛点，免费、开源，支持内网部署。

​		简而言之，YApi = 接口文档 + 接口调试 + mockserver + 自动化测试。

## 为什么用YApi？

​		相比较Rap，YApi对HTTP的支持更加全面，并且在提供文档托管能力的基础上，提供了接口调试的功能。

​		同时，利用单一数据源的机制，在调试接口的过程中，如果想修改接口定义，必须先修改接口文档，这一机制又保证了文档的时效性，能够防止出现后端自测完接口，文档忘记更新，导致前端白忙活的情况。

​		除此之外，YApi提供了极简的可视化操作界面，简单易用，功能强大，另外，基于插件机制和开放api，使得它的可扩展性非常高，可以满足各种定制化需求。

### 后端提效

​		YApi支持基于json5格式的请求体和响应体数据结构定义，相比较Rap的基于json-schema的方式，接口录入效率更高，json5格式也更加便于测试人员copy数据结构跑自己的测试用例，推荐使用。开启方法：选择项目-> 设置 -> 开启json5。

​		YApi内嵌了Chrome，可以直接基于文档发起http请求，并且能够根据接口定义预先设置好请求体数据，比单独利用postman等工具进行调试要更加高效。

### 前端提效

​		YApi提供了强大的Mock能力，在提供基本Mock能力的同时，还支持Mock期望的编写。

​		Mock期望是什么？Mock期望可以通过设置，根据不同请求参数返回不同的响应数据，也就是提供了可编程的动态Mock的能力，模拟真实响应再也不是难题。有了Mock期望功能，前端同学可以这么说：给我一份准确的接口文档，我能保证接口响应处理没有bug，联调？不存在的。

详见[Mock期望官方文档](https://hellosean1025.github.io/yapi/documents/adv_mock.html#mock-%E6%9C%9F%E6%9C%9B)

### 测试提效

​		据我所了解到的，目前测试人员一般是通过JMeter跑自动化测试用例，一般需要从外部粘贴预先写好的请求体进行用例编写，效率较低。

​		YApi提供了可视化的测试用例编写界面，不懂开发也能写用例，并且预设请求数据，无需重复录入，只需修改必要的数据即可。同时，YApi支持编写具有前后参数依赖的接口的测试用例，因此，用例也具备了可编程的动态测试能力，一个用例覆盖所有场景，再也不需要维护一大堆相似用例了。

详见[自动化测试官方文档](https://hellosean1025.github.io/yapi/documents/case.html)

### 关于联调

如果后端同学利用好YApi，开发完都自测确保定义的接口符合预期，前端利用好mock期望，我相信前端同学的工作将更加高效，Bug率也将更低，同时联调将会是非常薄的一层，如果配合好了说不定还能玩下持续集成（按接口维度集成，而不是版本）。
