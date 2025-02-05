Vagrant.configure("2") do |config|
  # Define a box genérica Debian 12
  config.vm.box = "reboxes/ubuntu2204"

  # Configurações do provedor VirtualBox
  config.vm.provider "virtualbox" do |vb|
    vb.name = "p01-diego-igor"  # Nome da VM no VirtualBox
    vb.memory = "1024"          # Memória RAM: 1024 MB
    vb.cpus = 1                 # Número de CPUs
    vb.gui = false              # Desativa a interface gráfica
  end

  # Configurações da máquina virtual
  config.vm.define "p01-diego-igor" do |aluno|
    aluno.vm.hostname = "p01-diego-igor"  # Configuração do hostname
    aluno.vm.network "private_network", ip: "192.168.57.10"  # Rede privada com IP estático

    # Adicionando discos adicionais
    (0..2).each do |i|
      aluno.vm.disk :disk, size: "10GB", name: "disk-#{i}"
    end

    # Caminho absoluto para o playbook
    aluno.vm.provision "ansible" do |ansible|
      ansible.playbook = "/home/ifpb/projetoAnsible/ansible/provision.yml"
      ansible.compatibility_mode = "1.8"       
    end
  end
end
