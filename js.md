## 1.从浏览器地址栏输入url到显示页面的步骤
### 简单版
1. 浏览器根据请求的URL交给DNS域名解析，找到真实IP，向服务器发起请求；
2. 服务器交给后台处理完成后返回数据，浏览器接收文件（HTML、JS、CSS、图象等）；
3. 浏览器对加载到的资源（HTML、JS、CSS等）进行语法解析，建立相应的内部数据结构（如HTML的DOM）；
4. 载入解析到的资源文件，渲染页面，完成。
### 详细版
1. 在浏览器地址栏输入URL
2. 浏览器查看缓存，如果请求资源在缓存中并且新鲜，跳转到转码步骤
```
   (1)如果资源未缓存，发起新请求
   (2)如果已缓存，检验是否足够新鲜，足够新鲜直接提供给客户端，否则与服务器进行验证。
   (3)检验新鲜通常有两个HTTP头进行控制Expires和Cache-Control：
    [1]HTTP1.0提供Expires，值为一个绝对时间表示缓存新鲜日期
    [2]HTTP1.1增加了Cache-Control: max-age=,值为以秒为单位的最大新鲜时间
```