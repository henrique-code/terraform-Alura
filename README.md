# Provisionamento de Instância EC2 com Terraform e Ansible (Alura)

Este projeto automatiza a criação de uma infraestrutura básica na AWS utilizando Terraform e ansible. O objetivo principal é subir uma instância EC2 de forma rápida e programática com um conteudo HTML gerado pelo ansible.

## 🚀 Tecnologias Utilizadas
* [Terraform](https://terraform.io)
* [AWS CLI](https://amazon.com)
* [Provedor AWS](https://terraform.io)
* [Ansible](https://docs.ansible.com/)

## 📋 Pré-requisitos
Antes de começar, você vai precisar:
1. Ter o **Terraform** instalado.
2. Ter o **Ansible** instalado.
3. Ter o **AWS CLI** configurado com suas credenciais (`aws configure`).
4. Uma conta ativa na AWS.

## 🔧 Como usar

1. **Clone o repositório:**
   ```bash
   git clone https://github.com/henrique-code/terraform-Alura
   cd terraform-Alura

2. **Alterar arquivo:**
   Alterar no arquivo main.tf o objeto "key_name" substituir pelo nome real da sua chave de acesso pem da AWS

3. **Inicie o Terraform:**
   ```bash
   terraform init
   ```

4. **Aplique a configuração:**
   ```bash
   terraform plan
   terraform apply
   ```
   
5. **Ronomei o ip do arquivo hosts:**
   E necessario alterar o ip do arquivo hosts, para o ipv4 da sua maquina da AWS
   
6. **Rode o ansible:**
   ```bash
   ansible-playbook playbook.yml -u ubuntu --private-key "sua key aqui.pem" -i hosts.yml
   terraform apply
   ```
7. **acessar instancia da aws:**
   Acessar a instancia via SSH, e verifique se o arquivo index.html foi criado.

