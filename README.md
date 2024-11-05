# haemosphere-vm-provision
# Step 1: Preparation
1. Create Virtual Machine on Nectar.
2. Install Ansible on your local terminal. <br />
   ```
   - Linux terminal (Ubuntu): sudo apt install ansible
   - Mac OS: pip install ansible
   - If you have Windows terminal, enable Windows Subsystem for Linux (WSL) and then use "sudo apt install ansible"
   ```
   If not work, follow the instructions on the offical document:
   https://docs.ansible.com/ansible/latest/installation_guide/index.html
3. Clone this repository to your local machine.<br />
    ```
    cd <your-working-directory>
    git clone https://github.com/quocthanhp/haemosphere-vm-provision.git
    ```
  
# Step 2: Run Ansible
1. Navigate to the project directory. <br />
   Ensure you are in the correct directory where you cloned the repository <br />
   ```
   cd <path-to-haemosphere-vm-provision>
   ```
3. Configure ```inventory.ini```.<br />
   - Change the value for ```ansible_host``` to your VM IP. <br />
   - Change the value for ```ansible_ssh_private_key_file``` to the path to your private key for accessing VM.
2. Run Ansible. <br />
   ```
   ansible-playbook -i inventory.ini provision_vm.yml
   ```
   It may take a few minutes for the process to complete.

# Step 3:  Enable persistent environment changes on VM
1. SSH into your VM.
2. Run ```source ~/.profile```.


