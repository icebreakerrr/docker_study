FROM rockylinux:9 

# RUN yum -y update && yum -y install vsftpd && yum clean alldo
RUN yum -y install vsftpd && yum clean all

COPY vsftpd.conf.rockylinux9.template /etc/vsftpd/vsftpd.conf
COPY WelcometoMyFTPServer.txt /var/ftp/pub/WelcometoMyFTPServer.txt

VOLUME [ "/var/ftp/pub" ]
EXPOSE 21 20

CMD [ "/usr/sbin/vsftpd" ]