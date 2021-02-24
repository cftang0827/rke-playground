# rke-playground
## Intro
Here is the playground for practicing k8s with rke, monitor with rancher and deploy a simple flask app to rke cluster. 

## Steps
1. Install Virtualbox in your machine
2. Install Vagrant for controlling your virtual machine, so we don't need to manage manually
    ```sh
    brew install --cask vagrant
    ```
3. Use `vagrant up` to create all virtual machine we are going to use for k8s. 
    ```sh
    # If you want to create only master1 machine for example
    vagrant up master1
    ```
4. Install ansible, it's the tool we can set up environment in VM(Virtual machine)
    ```sh
    ansible-playbook provision-vm.yml
    ```
5. After provision of the VM machine, we can set up RKE on those VM
    ```sh
    rke up
    ```