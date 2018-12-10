#### Koa2 vs Express
- Koa2只有一个核心的中间件模块，其他功能可作为可选中间件，这些中间件相互独立，而Express包含一个完整的应用框架，如路由和模板功能  
- Koa2用Context object(ctx)完全替换了NodeJs的req和res objects，可以用ctx.request和ctx.response调用，而Express只是对NodeJs的req和res objects进行了扩展  
- Koa2设计目的为提升写中间件的整体体验，使用async和await，减少写中间件的代码，而Express采用回调方式
- Koa2的性能略高于Express
  https://raygun.com/blog/koa-vs-express-2018/
  Software Versions Tested NodeJS v9.11.1 ExpressJS v4.16.3 Koa2 v2.5.0  

#### 结论
- 开始项目，并且可读性好，选择使用async/await的Koa2
- 如果有既存Express app，不要变了，Express和Koa2的ctx不兼容
- 性能考虑，koa2
- 轻量型应用，koa2
- 想使用一个完整的框架，不需要考虑过多依赖，Express