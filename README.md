This code is a fork from the original code by Jaganth outam (https://github.com/jaganthoutam/vicidial-install-scripts)

# Centos vididial Install pre_requisites

yum check-update

yum update -y

yum -y install epel-release

yum update -y

yum groupinstall 'Development Tools' -y

yum install git -y
yum install kernel*

#Disable SELINUX

sed -i 's/SELINUX=enforcing/SELINUX=disabled/g' /etc/selinux/config    

systemctl disable firewalld

reboot


# Install VICIDIAL

git clone https://github.com/liveafzal/ViciDial-install-on-CentOS7-using-scripts.git

cd ViciDial-install-on-CentOS7-using-scripts/


# Excute Centos vididial Install

chmod +x vicidial-install-centos7.sh

./vicidial-install-centos7.sh

