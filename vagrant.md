# Vagrant

# 01. A primeira máquina Virtual

- VirtualBox, VMware, Hyper-V, entre outros, são Hypervisors
- Um **Hypervisor** emula o hardware do computador para criar e executar máquinas virtuais
- O **Vagrant** é uma ferramenta que **controla** o Hypervisor a partir de um arquivo simples, o **Vagrantfile**
- O **Vagrantfile** define **detalhes da máquina virtual**, como o sistema operacional, a rede, software utilizado, etc
- O comando **vagrant init <box>** cria um Vagrantfile ex: vagrant init ***hashicorp/precise64***
- A box é baixada da internet e possui a imagem do sistema operacional, entre outras configurações
- Para inicializar e rodar a VM com Vagrant, usa-se o comando: **vagrant up**
- O comando **vagrant status** mostra detalhes sobre o status da máquina virtual
- Para se conectar com a máquina virtual, usamos a ferramenta **SSH**

 # 02. Configuração da Rede
  
  Existem 3 formas para configurar a rede:
  - **Forwarded Port**
  Na configuração Forwarded Port, mapeamos uma porta do host para o guest, por exemplo: config.vm.network "forwarded_port", guest: 80, host: 8080
  - **Private Network**
  Na Private Network (static ou dhcp) é usado um endereço privado que não é acessível na sua rede pública (por exemplo, a rede empresarial)
  - **Public Network**
  Na Public Network (static ou dhcp), usamos um endereço que faz parte da sua rede pública (por exemplo, da rede empresarial)
  
  - **vagrant halt** -- para a execução da MV
  - **vagrant reload** -- recarrega a configuração da máquina virtual
  - **vagrant destroy** -- destroy a MV criada pelo comando up
