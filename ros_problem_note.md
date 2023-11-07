1.当在topic 前面加上 / 的时候，无论在哪个命名空间底下，只会显示你所指定的  topic名字   
 	e.g. <odometryTopic>/$(arg bodyframe)/odom</odometryTopic>  
 		假设上述 topic在  ns = tb3_0下，若同上加上 / 则显示 /$(arg bodyframe)/odom, 若不加上则 显示 /tb3_0/$(arg bodyframe)/odom  
 		 
2.gazebo 启动一段时间后，robot会发生 偏移属于正常现象  

3.rviz 错误订阅话题会导致rviz闪退  

4.robot 闪现 瞬移到 世界map/world中心的问题解决：  
	可能原因是你的move_base参数和地图不适配，  
	考虑查看move_base速度/加速度是否过快，考虑更换地图，测试gmapping时候是否舜移  
	
