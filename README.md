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
--------------------------------------------------------------------------------
| DESCRIÇÃO |      IP      |  Nome do Host  |          FQDN          | Apelido |
--------------------------------------------------------------------------------
| VM1-PC1   | 192.168.13.1 | srv-vm1-pc1    | vm1pc1-913.ifalara.net | França  |
| VM2-PC1   | 192.168.13.2 | srv-vm2-pc1    | vm2pc1-913.ifalara.net | Italia  |
| VM1-PC2   | 192.168.13.3 | srv-vm1-pc2    | vm1pc2-913.ifalara.net |  Roma   |
| VM2-PC2   | 192.168.13.4 | srv-vm2-pc2    | vm2pc2-913.ifalara.net | Grecia  |
| VM1-PC3   | 192.168.13.5 | srv-vm1-pc3    | vm1pc3-913.ifalara.net |  Cuba   |
| VM2-PC3   | 192.168.13.6 | srv-vm2-pc3    | vm2pc3-913.ifalara.net | Mexico  |
| VM1-PC4   | 192.168.13.7 | VM1-PC4-Kelvin | VM1-PC4-Kelvin.net     | Brasil  |
| VM2-PC4   | 192.168.13.8 | VM2-PC4-Kelvin | VM2-PC4-Kelvin.net     | Holanda |
------------------------------------------------------------------------------
```

### **2) Definindo as Configurações de Hardware das VM's**

* Memória de Video: 16Mb
* Memória Principal: 512Mb
* Armazenamento: 10Gb

### **3) Criando os Diretórios**

3.1) Entrando no Usuário "redes"

```
sudo redes
```
<p><center> Figura 1:  Entrando no usuário "redes".</center></p>   
<img src="Imagens_Projeto913/Image1.png" alt="Imagens" title="Figura 1:  Entrando no usuário "redes"." width="500" height="auto" />

3.2) Verificar se possui os Diretórios

```
/labredes/images/original
/labredes/VM/913/<NomeDoAluno>
```

3.3) Criar os diretórios

* No nosso caso, é necessário

