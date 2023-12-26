---
title: 参数装饰器
order: 1
group:
  title: 装饰器
  order: 1
nav:
  title: 指南
---

<div style="text-align: center; font-size: xx-large;font-weight: bolder">参数装饰器</div> 

### ```@Params```

接收一个```js```对象，如```{a:1}```

使用方式：
```typescript
type Params = Record<string, any>

interface IData<D> {
    code: number,
    msg: string,
    data: D
}

interface Todo {
    id: number,
    name: string,
    date:number
}

@ReqComponent({baseURL : "http://example.com"})
class Todo {
  @Get('/mission/getDayMissions')
  async getTodoByDate(@Params dateParams:Params ): ReqReturnType<IData<Some>> {

  }

}
```
