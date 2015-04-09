# Install-Jenkins-on-Linux
Steps to Install Jenkins on Linux

1- Set the Proxy
        export ftp_proxy="<Proxy_Host>"
        export http_proxy="<Proxy_Host>"
        export https_proxy="<Proxy_Host>"

2- Add source in repository
        wget -q -O - http://pkg.jenkins-ci.org/debian/jenkins-ci.org.key | apt-key add -
        echo deb http://pkg.jenkins-ci.org/debian binary/ > /etc/apt/sources.list.d/jenkins.list
  
3- Install Jenkins
        apt-get update
        apt-get install jenkins
    
4- Log Location
        /var/log/jenkins/jenkins.log
    
5- Install Java
        Add repository
            add-apt-repository ppa:webupd8team/java
    
        Install Java
            apt-get update
            apt-get install oracle-java7-installer
    
        Update Alternatives
            update-alternatives --config java
            update-alternatives --config javac

6- Install Maven3
    add-apt-repository ppa:natecarlson/maven3
    apt-get update
    apt-get install maven3
    
7- Install Git
    apt-get install git-core
    
8- Generate SSH key
    ssh-keygen -t rsa -C "<email Id>"
  
