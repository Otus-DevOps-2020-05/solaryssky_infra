# solaryssky_infra
Задание # 5

bastion_IP = 130.193.39.78 
someinternalhost_IP = 10.130.0.12

5.1: Исследовать способ подключения к someinternalhost в одну команду на рабочем устройстве. 
    - используем jump: ssh -J dima@130.193.39.78 dima@10.130.0.12

5.2: Дополнительное задание: 
Дляподключения к хост с внутренним IP someinternalhost с локальной машины в файл ~/.ssh/config были добавлены строки:

Host bastion
	HostName 130.193.39.78
        User dima
	IdentityFile ~/.ssh/dima

Host someinternalhost
        HostName 10.130.0.12
        ProxyJump dima@130.193.39.78
        User dima

