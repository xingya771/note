* 添加用户并设置权限
```
rabbitmqctl stop_app
rabbitmqctl reset
rabbitmqctl start_app
rabbitmqctl add_user test test
rabbitmqctl add_vhost /
rabbitmqctl set_user_tags test administrator
rabbitmqctl set_permissions -p "/" test ".*" ".*" ".*"
```