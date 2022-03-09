# Vagrant 

Infraestrutura como código.
Cria ambientes para desenvolvimento.

![Vagrant icon!](vagrant.png "Vagrant")

## instalação:
sudo apt get virtualbox-qt
sudo apt get vagrant

## configuração:
mkdir ambiente_dev
cd ambiente_dev

## comandos
vagrant init hashicorp/precise64 --inicializa o Vagranfile baixando ambiente box 'precise64'

**Este comando cria tambem o Vagrantfile**

vagrant up -- subindo serviço
vagrant halt -- Para o serviço
vagrant status -- verificando status dos serviços ativos
vagrant ssh - conecta a VM
OBS: no windows pode ser usado o PuTTY

vagrant ssh-config -- verificar dados de conexao
vagrant ssh -p 2222 vagrant@127.0.0.1 --conectar no serviço

Obs: Hypervisor é o monitor de maquina virtual, é um processo que cria e executa maquinas virtuais.

Ex: Hyper-V, vSphere, Parallels, VMware, VirtualBox
Tipos de Hypervisors:
Tipo 1 ou Bare metal - executados diretamente no hardware do host ex: Hyper-V E vSphere
Tipo 2 Rodam com uma aplicação em cima do SO ex: VirtualBox e VMware
