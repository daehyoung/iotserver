# iotserver

## ssh server install

###  1. hosts.allow 에 182.161.173.230 추가 
    sudo gedit /etc/hosts.allow 

    # /etc/hosts.allow: list of hosts that are allowed to access the system.
    #                   See the manual pages hosts_access(5) and hosts_options(5).
    #
    # Example:    ALL: LOCAL @some_netgroup
    #             ALL: .foobar.edu EXCEPT terminalserver.foobar.edu
    #
    # If you're going to protect the portmapper use the name "rpcbind" for the
    # daemon name. See rpcbind(8) and rpc.mountd(8) for further information.
    #
    182.161.173.230


### 2. openssh server 설치 

    sudo apt-get install openssh-server
    sudo service ssh start
    sudo service ssh status


### 3. firewall 활성화 
    sudo ufw enable
    sudo ufw allow 22/tcp


### etc.

    https://www.st.com/resource/en/user_manual/dm00105262-developing-applications-on-stm32cube-with-rtos-stmicroelectronics.pdf



## docker install 

    sudo apt install docker.io

    sudo systemctl enable --now docker

    sudo usermod -aG docker $USER

    docker --version
