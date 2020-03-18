# Gitbook Booster
##  
  使用 Nginx 进行反向代理提升对文档的访问速度， 随后对于所有静态资源的 url 进行劫持，将静态资源转发至本服务不同的路由下，从而让 cdn 可以完成缓存，借此完成加速的目标。
  - 关于 js；css；font 等文件 均已转发至本地不同的路由。
  - 关于图片等文件，使用serverless来进行加载。
## 配置文件以及转发规则
所有配置文件的设置均在 conf.d 中。
对应参数为


| 域名 | 对应路由/serverless地址 |  
| - | - |
| static.gitbook.com | /static/ |      
| gstatic.gitbook.com | /gstatic/  | 
| blobscdn.gitbook.com | service-n14ldgzo-1255785256.hk.apigw.tencentcs.com/release/gitbookProxy |     
| gblobscdn.gitbook.com| service-2k76fzqg-1255785256.hk.apigw.tencentcs.com/release/gblobscdnProxy |
## 如何使用
将以下值修改为自己的参数:


