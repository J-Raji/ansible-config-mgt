#Install and configure Ansible on EC2 Instance

1.Update Name tag on your Jenkins EC2 Instance to Jenkins-Ansible

![Jenkins-Ansible Instance](./Images/jenkins-ansible.png)

2.In your GitHub account create a new repository and name it ansible-config-mgt

![ansible-config-mgt repo](./Images/repo.png)

[]Jenkins-ansible instance

![Jenkins-Ansible launched](./Images/instance.png)

3.Install Ansible

`sudo apt update`

`sudo apt install ansible`

![Install ansible done](./Images/ansible.png)


[]Check your Ansible version by running 
`ansible --version`

![check ansible version](./Images/version.png)

4.Configure Jenkins build job to save your repository content every time you change it

-Jenkins page 15.228.170.184:8080
-admin password d84735f4243e4faf8ea684558518804e

[]Create a new Freestyle project ansible in Jenkins and point it to your ‘ansible-config-mgt’ repository

![ansible freestyle project created](./Images/ansible-freestyle-project.png)

[]Configure Webhook in GitHub and set webhook to trigger ansible build
-Repository https://j-raji.github.io/ansible-config-mgt/
-Webhook http://15.228.170.184:8080/github-webhook

![webhook created](./Images/ansible-webhook.png)

[]Configure a Post-build job to save all (**) files

![ansible settings](./Images/ansible-setting.png)

