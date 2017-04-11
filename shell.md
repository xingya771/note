* 杀掉特定进程
```
kill -9 $(pwdx `ps -ef |grep python |grep -v "grep"|awk '{print $2}'`|grep "giraffe"|awk -F "[:]" '{print $1}')
```
2. 查询内存使用最高的10个进程
```
 ps aux | sort -k4nr | head -n 10
 ps axu | head -n 10
```
3. 