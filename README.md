# solaryssky_infra
������� # 5

bastion_IP = 130.193.39.78 
someinternalhost_IP = 10.130.0.12

5.1: ����������� ������ ����������� � someinternalhost � ���� ������� �� ������� ����������. 
    - ���������� jump: ssh -J dima@130.193.39.78 dima@10.130.0.12

5.2: �������������� �������: 
�������������� � ���� � ���������� IP someinternalhost � ��������� ������ � ���� ~/.ssh/config ���� ��������� ������:

Host bastion
	HostName 130.193.39.78
        User dima
	IdentityFile ~/.ssh/dima

Host someinternalhost
        HostName 10.130.0.12
        ProxyJump dima@130.193.39.78
        User dima

