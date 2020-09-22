# conda命令无法更新_解决方案

> 问题1：终端输入anaconda-navigator，一直卡在loading applications，并且终端显示<urlopen error [Errno -2] 未知的名称或服务>

> 问题2：终端输入conda upgrade anaconda-navigator，显示CondaHTTPError: HTTP 000 CONNECTION FAILED for url <https://repo.anaconda.com/pkgs/r/noarch/repodata.json.bz2>，但是我是有网络代理代理的(SSR)

## 错误解决方案（前车之鉴）

一开始以为是下载源的问题，后来换了清华、中科大、上交源都发现没用，就以为是anaconda自身的问题。
后来痛心重装anaconda，发现问题还是未解决。
