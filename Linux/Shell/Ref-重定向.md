
## Linux Shell环境中的重定向

- 输入输出重定向用符号<和>来表示
- 0、1和2分别表示标准输入、标准输出和标准错误

### Sample

1.重定向标准输出到文件
`cat foo > foo.txt`

2.重定向标准错误到文件
`cat foo 2> foo.txt`

3.重定向标准输出到标准错误
`cat foo 1>&2`

4.重定向标准错误到标准输出
`cat foo 2>&1`

5.重定向标准输出，标准错误到同一个文件
`cat foo > foo.txt 2>&1或cat foo &> foo.txt`

这里第个顺序很重要，先把标准输出重定向到文件，再把标准错误输出到标准输出，因为标准输出已经重定向到文件，所以标准错误与重定向到文件

\>&与&>效果相同

资料来源：[linux 重定向 标准错误与标准输出到同一文件][1]

[1]:http://blog.chinaunix.net/uid-21142030-id-3211182.html