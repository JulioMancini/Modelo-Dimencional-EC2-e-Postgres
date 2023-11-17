# MODELO DIMENCIONAL
Objetivo = Criar, popular e testar modelo Dimensional básico para testes SQL
# Criando e configurando uma instância no EC2
* Procurar por EC2 na pesquisa

![foto ec2 1](https://github.com/JulioMancini/Modelo_Relacional-EC2-e-Postgres/assets/145502330/50938737-04f6-4bfc-8245-0d87b9aa43bf)


* procurar por instância e criar uma em Executar instância
* Criar um nome para instância
* escolher uma versão não tão atualizada (versão escolida: Ubuntu Serve 20.04 LTS (HMV), SSD Volume Type) versão gratuita

  ![ec2 2](https://github.com/JulioMancini/Modelo_Relacional-EC2-e-Postgres/assets/145502330/f9f0541d-203c-4e53-a075-8ea58c168c10)

* Arquitetura 64(x68)
* Tipo de instância não precisa alterar ( continuar com t2.micro)
* Criar uma chave
* permitir tráfego SSH
* Após a criação execute a instancia e salve a chave para poder fazer o acesso em SSH no Shell da maquina

![ec2 3](https://github.com/JulioMancini/Modelo_Relacional-EC2-e-Postgres/assets/145502330/3027e9ad-0b9f-441e-be8a-7c9cc988d9f8)

* Abra o Shell da maquina e posicione no diretório onde a chave está.
* Copiar e colar o comando (chave) diretamente do site da AWS

![ec2 4](https://github.com/JulioMancini/Modelo_Relacional-EC2-e-Postgres/assets/145502330/9997509b-8114-4d32-b5aa-74737ac3afbd)

[Pronto, agora voçê está conectado ao Linux e Ubuntu que está rodando em um servidor do AWS]![ec2 5](https://github.com/JulioMancini/Modelo_Relacional-EC2-e-Postgres/assets/145502330/5b33745e-7454-4777-b3a8-1f43635370c9)

# Instalando e configurando o Postgres
**Atualizar o unzip**
```bash
sudo apt-get install unzip
```
**Instalar postgres e criar config do repositório**
```bash
sudo sh -c 'echo "deb http://apt.postgresql.org/pub/repos/apt $(lsb_release -cs)-pgdg main" > /etc/apt/sources.list.d/pgdg.list'
```
**Importar chave**
```bash
wget --quiet -O - https://www.postgresql.org/media/keys/ACCC4CF8.asc | sudo apt-key add -
```
**Atualizar pacotes**
```bash
sudo apt-get update
```
**Instala última versão do postgres**
```bash
sudo apt-get -y install postgresql
```
**Mudar para usuario postres**
```bash
sudo su - postgres
```
