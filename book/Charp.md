# C#常用代码

#### 1. WebAPI中获取项目根目录
``` charp
  //方式一：
  Server.MapPath("~/");
  
  //方式二：
  using System.Web.Hosting;
  
  string rooturl = HostingEnvironment.MapPath("~/");
```

#### 2. List根据字段属性去重
``` charp
    List<T> listresult = List.Where((x,i)=>List.FindIndex(z=>z.SYS_ID==x.SYS_ID)==i).ToList();
```
