# redis-local-replication-cluster

This example explains you how to run servers locatlly to and convert them into master slave mode . Also how automatically che ild node changes to master if master die . 

Follow the following steps to run all the servers instances . 

1) Install redis server redis-4.0.14 . we are running every on this version of redis- server  

2) We are running every server on the following ports 7001 , 7002 , 7003 , 7004 , 7005 , 7006 

redis-server node1.conf 
redis-server node2.conf 
redis-server node3.conf 
redis-server node4.conf 
redis-server node5.conf 
redis-server node6.conf 

3) ./redis-trib.rb create --replicas 1 127.0.0.1:7001 127.0.0.1:7002 127.0.0.1:7003 127.0.0.1:7004 127.0.0.1:7005 127.0.0.1:7006

4) Now you can see one will be master server and other will be slave servers . Now stop the master server and you will see automatically it will promote one of the slave server as master 


