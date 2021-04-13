# Vagrant-CICD
Vagrant CI/CD experiment.

## GitHub actions
This short experiment is to create a CI/CD pipeline for a Vagrantfile. The pipeline is located in the "workflows" directory and it is running as "self-hosted" which means I have my own AWS Windows server running the pipeline instead of the default GitHub containers(that might sound complex but it's actually very easy to achieve). 

This pipeline is intended to create artifacts out of the Vagrantfile automagically, in this case **ggcore.box** and **ggcore.ova**, which you could upload to your repository of preference, like Nexus or Artifactory.

Requirements:
* AWS (or any other public cloud).
* Windows server with VirtualBox and Vagrant installed.
* The correct security groups.
* Add the server as [self-hosted runner.](https://docs.github.com/en/actions/hosting-your-own-runners/adding-self-hosted-runners)
* Create the pipeline as shown in this example repository.

Voilá, your pipeline is ready to use!

Note: During my experiment I realized Windows it's actually better to handle nested virtualization than Linux, and that's the reason behind using a Windows server in AWS.
