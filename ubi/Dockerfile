FROM registry.access.redhat.com/ubi7/ubi
MAINTAINER M. Kerker marcel.kerker@hcs-company.com
ADD ./init.sh ./
RUN yum install nmap-ncat --disablerepo=* --enablerepo=rhel-7-server-rpms -y && yum clean all -y 
RUN chown 1001:1001 init.sh && chmod o+w init.sh
USER 1001
EXPOSE 8080
CMD ["./init.sh"]
