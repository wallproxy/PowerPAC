PowerPAC
===
自动生成/更新高效、强大的PAC

gfwlist.ini是对于AutoProxy规则的演示配置文件，功能与AutoProxy扩展等效；  
gfwlist.bat是以gfwlist.ini为profile生成/更新gfwlist.pac的批处理；  

iplist.ini是对于ip列表规则的演示配置文件，功能是国内ip不走代理国外ip走代理；  
iplist.bat是以iplist.ini为profile生成/更新iplist.pac的批处理；  

如果需要在非Win平台通过命令行更新PAC，可使用以下格式的命令：

    $ python2 /home/user/PowerPAC/startup.py pac gfwlist.ini gfwlist.pac
    $ python2 /home/user/PowerPAC/startup.py pac iplist.ini iplist.pac

如果需要在Win平台自动定期更新，使用计划任务执行上述*.bat即可；  
如果需要在非Win平台自动定期更新，将上述命令添加到crontab即可。  

更复杂的代理需求可通过修改proxy.ini进一步实现，应该是可以覆盖任意代理需求的；  
如果需求确实复杂到无法通过定制url或ip规则，可以自己修改生成的PAC，修改会在更新时保留；  
通过智能代理功能可以做到一些PAC无法做到的事情，也可以PAC与智能代理配合使用，详情请参考https://code.google.com/p/wallproxy/wiki/PAC
