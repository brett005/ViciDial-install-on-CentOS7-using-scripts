# ViciDial-install-on-CentOS7-using-scripts

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

git clone https://github.com/liveafzal/vicidial-install-centos7.git

cd vicidial-install-scripts

# Excute Centos vididial Install

chmod +x vicidial-install-centos7.sh

./vicidial-install-centos7.sh

