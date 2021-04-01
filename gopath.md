gopath 就是开发者存放所有go项目的目录

go官方把gopath称为工作空间

go安装之后会指定一个默认的工作空间
gopath=/c/users/water/go
但是这个默认的gopath还只是go的一个属性
你可以通过 go env GOPATH 查看它的值
你也在操作系统中设置GOPATH=$(go env GOPATH)属性，就像java的JAVA_HOME一样
同时你在系统的环境变量中把$GOPATH/bin目录配进去
这样你的项目生成的二进制文件，就可以在任何地方运行了

go建议开发者把所有go项目放在$gopath/src/你的项目下

所有项目生成的二进制文件放在$gopath/bin/具体的可执行文件

当go程序编写完成之后，你可以通过go install gopath/src/youProject/package
来安装二进制文件到gopath/bin目录下
值得注意的是如果你的操作系统没有设置GOPATH环境变量，那么程序会安装到$(go env GOROOT)目录下(/c/users/water/local/go)