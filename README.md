# Projeto de Provisionamento com Vagrant e Ansible

## Integrantes
- Nome01 (Diego Costa Sales)
- Nome02 (Igor de Oliveira Teixeira)

## Disciplina
- Administração de Sistemas Abertos
- Professor: Pedro Filho

## Descrição do Projeto
Este projeto utiliza Vagrant e Ansible para provisionar e configurar automaticamente uma máquina virtual com as seguintes características:
- Box: debian/bookworm64
- **Configuração**:
  - Memória RAM: 1024 MB
  - 3 discos adicionais de 10 GB
  - Rede privada e pública
- **Configurações Automatizadas**:
  - Atualização do sistema operacional
  - Configuração de hostname
  - Criação de usuários e grupos
  - Configuração de sudo
  - Configuração de autenticação SSH por chaves
  - Configuração de LVM e NFS
  - Monitoramento de acessos

## Como Executar
1. Clone o repositório:
   ```bash
   git clone https://github.com/diegosls/projetoAnsible.git
   cd vagrant-ansible-provisioning
