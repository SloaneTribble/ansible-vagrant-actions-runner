# -*- mode: ruby -*-
# vi: set ft=ruby :
# The above lines are modelines for text editors. The first line is for Emacs and the second for Vim.
# They tell the editor to use Ruby mode, optimizing syntax highlighting and indentation rules for Ruby code.

Vagrant.configure("2") do |config|
  # This line configures the Vagrant environment. "2" refers to the API version for the configuration object.
  # This ensures that you use the correct set of features and syntax supported in Vagrant version 2.

  config.vm.box = "bento/ubuntu-20.04"
  # This sets the base image (or "box") for the virtual machine (VM). Here, it uses "bento/ubuntu-20.04",
  # which is a standard Ubuntu 20.04 image provided by Bento, a project offering minimal Vagrant base boxes.

  config.vm.provision "ansible" do |ansible|
    # This block configures provisioning for the VM using Ansible.
    # "ansible" is a string arg passed to the provision method, indicating type of provisioner to use
    # do |ansible| ...end is a Ruby block performing operations on the configuration object for the Ansible provisioner, which here is named "ansible" via |ansible|

    ansible.verbose = "v"
    # Sets the verbosity level of Ansible. Here, "v" corresponds to verbose output, which means more detailed
    # output will be shown during the Ansible run. 

    ansible.playbook = "playbook.yaml"
    # Specifies the Ansible playbook file to be used. 
  end
end
