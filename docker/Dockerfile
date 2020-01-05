# =============================================================================
#
# CentOS-7 7.6.1810 x86_64
# 
# =============================================================================
FROM centos:centos7.6.1810

RUN \
    curl -o /etc/yum.repos.d/CentOS-Base.repo http://mirrors.aliyun.com/repo/Centos-7.repo && \
    curl -o /etc/yum.repos.d/epel.repo http://mirrors.aliyun.com/repo/epel-7.repo && \
    ln -sf /usr/share/zoneinfo/Asia/Shanghai /etc/localtime && \
    yum -y install make gcc gcc-c++ nodejs && yum clean all && \
    npm config set registry https://registry.npm.taobao.org && \
    npm install -g log.io --user "root"

WORKDIR /root/.log.io/

CMD ["log.io-harvester"]