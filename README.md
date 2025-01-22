# Ansible
1. Update the System Packages
sudo yum update -y

2. Install the EPEL Repository
sudo amazon-linux-extras install epel -y

3. Install Ansible
sudo yum install ansible -y

4. Verify Ansible Installation
ansible --version

5. Optional: Install Python 3 Support
sudo yum install python3 python3-pip -y
sudo pip3 install ansible

6. Testing Ansible
ansible localhost -m ping


To establish SSH connection in both master and worker nodes
vi sshd_config
[#PermitRootLogin yes -> remove"#"]
[PasswordAuthentication no -> set to yes]

cd /etc/ansible

ssh-keygen  -> enter 3 times

cd .ssh

cat id_rsa.pub  [copy the code, paste in nodes]

In worker nodes
cd .ssh

vi authorized_keys [paste code here]

To check in master 

ansible -m ping node pvt ip