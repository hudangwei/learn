centos6.5 ��װdocker
1.�鿴ϵͳ�汾��
lsb_release -a
2.�鿴�ں˰汾
uname -a
3.yum��ʽ�����ںˣ���ΪDocker�Ƽ�ʹ��3.8�����ںˣ�
rpm --import https://www.elrepo.org/RPM-GPG-KEY-elrepo.org
rpm -Uvh http://www.elrepo.org/elrepo-release-6-6.el6.elrepo.noarch.rpm
yum --enablerepo=elrepo-kernel install kernel-lt -y
4.�޸��ں�������
vi /etc/grub.conf �°�װ���ں�һ���ڵ�һ��,�����default = 1 ��Ϊ default = 0
5.����ϵͳ
reboot
6.�鿴�ں���Ϣ
uname -r

7.��װdocker
yum install -y epel-release
yum install -y docker-io

docker version

docker -d

