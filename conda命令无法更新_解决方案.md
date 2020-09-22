# conda命令无法更新_解决方案

> 问题1：终端输入```anaconda-navigator```，一直卡在loading applications，并且终端显示<urlopen error [Errno -2] 未知的名称或服务>

> 问题2：终端输入```conda upgrade anaconda-navigator```，显示CondaHTTPError: HTTP 000 CONNECTION FAILED for url <https://repo.anaconda.com/pkgs/r/noarch/repodata.json.bz2>，但是我是有网络代理代理的(SSR)

## 错误解决方案（前车之鉴）

一开始以为是下载源的问题，后来换了清华、中科大、上交源都发现没用，就以为是anaconda自身的问题。  
后来痛心重装anaconda，发现问题还是未解决。（于是心态开始发生了一些变化，我的python环境全没了）  

## 正解

然后深夜突然发现知乎上一个博客，恍然大误。我有代理，那么用官方源应该也没问题啊，那我把代理关了，用国内镜像源也应该不成问题呀，为什么都无法链接到服务器呢？  

于是用```env | grep -i proxy```查看系统与代理有关的环境变量，发现与ssr里面配置的代理设置一致，
