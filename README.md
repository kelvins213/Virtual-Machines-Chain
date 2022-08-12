## **Projeto De Redes Do Segundo Bimestre**

### **1) Definindo as Configurações de Redes**

```
Tabela 1: Definições de endereços IPs da Rede e Nomes de Hosts
------------------------------------------------------------------------
|  DESCRICAO  |       IP         |             HOSTNAME                |
-----------------------------------------------------------------------|
| rede        | 192.168.13.0     |                                     |
| máscara     | 255.255.255.240  |                                     |
| Gateway     | 192.168.13.16    |                                     |
| VM1-PC1     | 192.168.13.1     |   vm1pc1-913-grupo1.ifalara.net     |
| VM2-PC1     | 192.168.13.2     |   vm2pc1-913-grupo1.ifalara.net     |
| VM1-PC2     | 192.168.13.3     |   vm1pc2-913-grupo1.ifalara.net     |
| VM2-PC2     | 192.168.13.4     |   vm2pc2-913-grupo1.ifalara.net     |
| VM1-PC3     | 192.168.13.5     |   vm1pc3-913-grupo1.ifalara.net     |
| VM2-PC3     | 192.168.13.6     |   vm2pc3-913-grupo1.ifalara.net     |
| VM1-PC4     | 192.168.13.7     |   vm1pc4-913-grupo1.ifalara.net     |
| VM2-PC4     | 192.168.13.8     |   vm2pc4-913-grupo1.ifalara.net     |
------------------------------------------------------------------------
```

```
Tabela 1: Configurações de IPs da Rede e Nomes de Hosts
-------------------------------------------------------------------------------------------------
| DESCRIÇÃO |      IP      |  Nome do Host   |          FQDN                          | Apelido |
-------------------------------------------------------------------------------------------------
| VM1-PC1   | 192.168.13.1 | VM1-PC4-Julio   | VM1-PC1-Julio.grupo1-913.ifalara.net   | França  |
| VM2-PC1   | 192.168.13.2 | VM2-PC1-Julio   | VM2-PC1-Julio.grupo1-913.ifalara.net   | Italia  |
| VM1-PC2   | 192.168.13.3 | VM1-PC2-Daniel  | VM1-PC2-Daniel.grupo1-913.ifalara.net  |  Roma   |
| VM2-PC2   | 192.168.13.4 | VM2-PC2-Daniel  | VM2-PC2-Daniel.grupo1-913.ifalara.net  | Grecia  |
| VM1-PC3   | 192.168.13.5 | VM1-PC3-Ricardo | VM1-PC3-Ricardo.grupo1-913.ifalara.net |  Cuba   |
| VM2-PC3   | 192.168.13.6 | VM2-PC3-Ricardo | VM2-PC3-Ricardo.grupo1-913.ifalara.net | Mexico  |
| VM1-PC4   | 192.168.13.7 | VM1-PC4-Kelvin  | VM1-PC4-Kelvin.grupo1-913.ifalara.net  | Brasil  |
| VM2-PC4   | 192.168.13.8 | VM2-PC4-Kelvin  | VM2-PC4-Kelvin.grupo1-913.ifalara.net  | Holanda |
-------------------------------------------------------------------------------------------------
```

### **2) Definindo as Configurações de Hardware das VM's**

* Memória de Video: 16Mb
* Memória Principal: 512Mb
* Armazenamento: 10Gb

### **3) Criando os Diretórios**

#### 3.1) Entrando no Usuário "redes"

```
su redes
```
<p><center> Figura 1:  Entrando no usuário "redes".</center></p>   
<img src="Imagens_Projeto913/image1.png" alt="Imagens" title="Figura 1:  Entrando no usuário "redes"." width="500" height="auto" />

<p><center> Figura 2:  Entrando no usuário "redes" - Inserindo a Senha.</center></p>   
<img src="Imagens_Projeto913/image14.png" alt="Imagens" title="Figura 2:  Entrando no usuário "redes" - Inserindo a Senha." width="500" height="auto" />

#### 3.2) Verificar se possui os Diretórios

```
/labredes/images/original
/labredes/VM/913/<NomeDoAluno>
```

#### 3.3) Criar os diretórios

* No nosso caso, é necessário criar os diretórios /labredes /VM /913 /fulano.
* Para isso, basta utilizar o comando "sudo mkdir" e o nome do diretório.

```
sudo mkdir labredes
```
<p><center> Figura 3:  Criando o Diretório /labredes.</center></p>   
<img src="Imagens_Projeto913/image17.png" alt="Imagens" title="Figura 3:  Criando o Diretório /labredes." width="500" height="auto" />


```
sudo mkdir VM
```
<p><center> Figura 4:  Criando o Diretório /VM.</center></p>   
<img src="Imagens_Projeto913/image27.png" alt="Imagens" title="Figura 3:  Criando o Diretório /VM." width="500" height="auto" />

```
sudo mkdir 913
```
<p><center> Figura 5:  Criando o Diretório /913.</center></p>   
<img src="Imagens_Projeto913/image22.png" alt="Imagens" title="Figura 3:  Criando o Diretório /913." width="500" height="auto" />

```
sudo mkdir fulano
```
<p><center> Figura 6:  Criando o Diretório /fulano.</center></p>   
<img src="Imagens_Projeto913/image19.png" alt="Imagens" title="Figura 3:  Criando o Diretório /fulano." width="500" height="auto" />


#### 3.4) Adicionar o usuário "aluno" no grupo "redes"

```
sudo usermod -aG redes aluno
```
<p><center> Figura 7:  Adicionando "aluno" em "redes".</center></p>   
<img src="Imagens_Projeto913/image20.png" alt="Imagens" title="Figura 7:  Adicionando "aluno" em "redes"." width="500" height="auto" />

<p><center> Figura 8:  Adicionando "aluno" em "redes" - Inserindo Senha.</center></p> 
<img src="Imagens_Projeto913/image39.png" alt="Imagens" title="Figura 8:  Adicionando "aluno" em "redes" - Inserindo Senha." width="500" height="auto" />

* Modificar o dono da pasta labredes para o usuario nobody e grupo nogroup

```
sudo chown -R nobody:nogroup /labredes
```
<p><center> Figura 9: Modificando o dono da Pasta</center></p> 
<img src="Imagens_Projeto913/image43.png" alt="Imagens" title="Figura 9: Modificando o dono da Pasta" width="500" height="auto" />

* Alterando o proprietário de grupo do diretório /labredes para o grupo redes

```
sudo chgrp -R redes /labredes
```
<p><center> Figura 10: Alterando o proprietário</center></p> 
<img src="Imagens_Projeto913/image41.png" alt="Imagens" title="Figura 10: Alterando o proprietário" width="500" height="auto" />

* Alterando as permissões do diretório para escrita pelos membros do grupo
```
sudo chmod -R 771 /labredes 
```
<p><center> Figura 11: Alterando as permissões dos diretórios</center></p> 
<img src="Imagens_Projeto913/image24.png" alt="Imagens" title="Figura 11: Alterando o proprietário -R 771" width="500" height="auto" />

* Listando os Grupos
```
getent group
```
<p><center> Figura 12: Listando os Grupos</center></p> 
<img src="Imagens_Projeto913/image31.png" alt="Imagens" title="Figura 12: Listando os Grupos" width="500" height="auto" />

<p><center> Figura 12.1: Listando os Grupos</center></p> 
<img src="Imagens_Projeto913/GetentGroup.png" alt="Imagens" title="Figura 12.1: Listando os Grupos" width="800" height="auto" />


### **4) Criando as VM's**

#### 4.1) Importando o Arquivo

* No VirtualBox, ir na aba ```Arquivos```, na segunda opção ```Importar Appliance```.

<p><center> Figura 13: Importando Appliance</center></p> 
<img src="Imagens_Projeto913/image36.jpg" alt="Imagens" title="Figura 13: Importando Appliance" width="500" height="auto" />

* Na aba ```Importar Appliance```, deve-se inserir o diretório ```/labredes/images/original/ubuntu-server-mini.ova```.
* Nas configurações de Pasta Padrão, deve-se inserir o diretório ```/labredes/VM/913/fulano```.

<p><center> Figura 14: Importando Appliance - Configurações</center></p> 
<img src="Imagens_Projeto913/image40.png" alt="Imagens" title="Figura 14: Importando Appliance - Configurações" width="800" height="auto" />

* Após as edições, clicar em ```Importar```.

#### 4.2) Definindo as configurações de Rede

* Selecionar a VM recem-criada e ir em ```Configurações``` -> ```Rede```.
* Habilitar Placa de Rede.
* Criar a Rede Interna.
* Ir em ```Avançado``` e alterar o Endereço MAC.

<p><center> Figura 15: Configurações de Rede das VM's</center></p> 
<img src="Imagens_Projeto913/image5.png" alt="Imagens" title="Figura 15: Configurações de Rede das VM's" width="800" height="auto" />

<p><center> Figura 16: Configurações de Rede das VM's - MAC</center></p> 
<img src="Imagens_Projeto913/image18.png" alt="Imagens" title="Figura 16: Configurações de Rede das VM's - MAC" width="800" height="auto" />

#### 4.3) Repetir os Passos Anteriores

* Repetir os passos anteriores para criar a segunda VM.
* Caso Tenha feito tudo corretamente, ambas as VM's deverão funcionar.

<p><center> Figura 17: VM's funcionando</center></p> 
<img src="Imagens_Projeto913/image3.png" alt="Imagens" title="Figura 17: VM's funcionando" width="800" height="auto" />

### **5) Configurando o NETPLAN**

* Utilizando o comando sudo nano.

```sudo nano /etc/netplan/01-netcfg.yaml```

* Após, inserir os IP's de acordo com a tabela.

```
   network:
     version: 2
     renderer: networkd
     ethernets:
       enp0s3:                           # nome da interface que está sendo configurada. Verifique com o comando 'ifconfig -a'
         addresses: [192.168.13.<numeroVM1-PC1>/28]    # IP e Máscara do Host.
         gateway4: 192.168.13.1          # IP do Gateway
         dhcp4: false                  # dhcp4 false -> cliente DHCP está desabilitado, logo o utilizará o IP do campo 'addresses'
 ```
         
* Após, aplicar as configurações utilizando o comando ```sudo netplan apply```.

<p><center> Figura 18: Netplan</center></p> 
<img src="Imagens_Projeto913/image32.png" alt="Imagens" title="Figura 18: Netplan" width="600" height="auto"/>

### **5) Instalação e Configuração do SSH**

* Inserir os comandos para as atualizar as definições e pacote do ubuntu

```
sudo apt update       
sudo apt upgrade -y 
```

* Após, instalar o SSH, para isso utilize o comando ```sudo apt-get install openssh-server```
* Após o processo, dar o comando ```systemctl status ssh``` para verificar o status do ssh

<p><center> Figura 19: Instalando o SSH</center></p> 
<img src="Imagens_Projeto913/image21.png" alt="Imagens" title="Figura 19: Instalando o SSH" width="600" height="auto"/>

<p><center> Figura 20: Verificando o Status do SSH</center></p> 
<img src="Imagens_Projeto913/image25.png" alt="Imagens" title="Figura 20: Verificando o Status do SSH" width="600" height="auto"/>

* Verificar o Status das Portas do Sistema, para isso utilize o comando ```netstat -an | grep LISTEN.```

<p><center> Figura 21: Verificando o Status das Portas do Sistema</center></p> 
<img src="Imagens_Projeto913/image35.png" alt="Imagens" title="Figura 21: Verificando o Status das Portas do Sistema" width="600" height="auto"/>

* Ativar o UFW, para isso deve-se utilizar o comando ```sudo ufw allow ssh.```

<p><center> Figura 22: Ativando o UFW</center></p> 
<img src="Imagens_Projeto913/image2.png" alt="Imagens" title="Figura 22: Ativando o UFW" width="600" height="auto"/>

* Verificar o status UFW , para isso deve-se utilizar o comando ```sudo ufw status```
* Ativar o UFW, utilizando o comando ```sudo ufw enable```

<p><center> Figura 23: Verificando e Ativando o UFW</center></p> 
<img src="Imagens_Projeto913/image26.png" alt="Imagens" title="Figura 23: Verificando e Ativando o UFW" width="600" height="auto"/>

* Após todo o processo, ao conectar, esta tela deve ser exibida.

<p><center> Figura 24: SSH conectado </center></p> 
<img src="Imagens_Projeto913/image16.png" alt="Imagens" title="Figura 24: SSH conectado" width="600" height="auto"/>
