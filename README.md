### Setup an ubuntu local server with Jenkins instance and Git

#### Step 1: Check the repos out

    cd /ROOT
    git clone https://github.com/ninique-sfpl/jenkins-remote-deployment.git jenkins

#### Step 2: Update Vagrantfile

You can update the IP address and forwarded port:

    config.vm.network "private_network", ip: "192.168.53.18"
    config.vm.network "forwarded_port", guest: 80, host: 9090

#### Step 3: Run Vagrant up

     cd jenkins 
     vagrant up


### Jenkins

#### Setup Jenkins configurations

##### Launch Jenkins on a browser at http://ip-address:8080

##### Unlock Jenkins

    vagrant ssh
    
  login to the server from a terminal as jenkins 

    sudo su jenkins
    cd ~
    cat secrets/initialAdminPassword

  Copy the password into the Administrator 

##### Customize Jenkins
  > Install suggested plugins
  
##### Create First Admin User
  Complete the form
  - username: admin

##### Jenkins is ready
  > Start using Jenkins
  
##### You should get to the following Jenkins dashboard:
![Jenkins Dashboard](https://github.com/ninique-sfpl/jenkins-remote-deployment/blob/master/docs/img/welcome.png)

