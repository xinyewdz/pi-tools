安装samba服务
#启用samba
sudo apt install samba samba-common-bin
cat /etc/samba/smb.conf
[public]
comment = Public Storage
path = /home/pi/data/TDDOWNLOAD
read only = no#任何人都具有了访问修改的权限
#因为是公共文件夹，所以给了所有用户全部权限，可以自定义
create mask = 0777#新创建文件的默认属性
directory mask = 0777#新创建文件夹的默认属性
guest ok = yes#默认的访问用户名为guest
browseable = yes

#将系统用户添加到smb系统
sudo smbpasswd -a pi
#激活用户
sudo smbpasswd -e pi
#重启
sudo smb restart
