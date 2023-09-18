---
title: 示例
order: 2
group:
  title: 基础
  order: 1
nav:
  title: 指南
---

<div style="text-align: center; font-size: xx-large;font-weight: bolder">请求示例</div> 

注意： req4d使用**esm**：

```import { ReqComponent } from "req4d"```

## 使用```@ReqComponent```标记一个类为请求类

```typescript
@ReqComponent(baseUrl = "http://example.com")
class User {

}
```

## 使用```@Get```标记方法需要进行get请求

```typescript
@ReqComponent(baseUrl = "http://example.com")
class User {
  @Get('/user')
  async getUser(): ReqReturnType<UserType> {

  }

}
```

## 使用请求后的数据

```typescript
const userInstance = new User();

userInstance.getUser().then((user) => {
  //do something
})
```

注意：上文中```Promise resolve```的```user```数据类型在请求函数```getUser```的返回值中```ReqReturnType<UserType>```进行标记，标记后可以获得类型```UserType```的类型推断


