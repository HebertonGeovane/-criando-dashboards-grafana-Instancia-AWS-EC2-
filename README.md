# Criando Dashboards Grafana Instancia AWS EC2

## pré-requisitos

Conta AWS: https://lnkd.in/dDaqthFy

Usuário IAM : https://lnkd.in/dKHpZaKi

Configure Access Key , Secret Key AWS e  Região AWS .

☑️ Acesse sua Instância EC2

 Security Group,  Adicionar Regra de Entrada 

Custom TCP.

TCP

Port Range 3000



☑️ Atualizar os Pacotes

sudo apt update



☑️ Instalar os Pacotes Pré-Requisitos

sudo apt-get install -y apt-transport-https software-properties-common wget



☑️ Crie o diretório e importe a chave GPG
```
sudo mkdir -p /etc/apt/keyrings/

wget -q -O - https://apt.grafana.com/gpg.key | gpg --dearmor | sudo tee /etc/apt/keyrings/grafana.gpg > /dev/null
```


☑️ Adicione o repositório do Grafana
```
echo "deb [signed-by=/etc/apt/keyrings/grafana.gpg] https://apt.grafana.com stable main" | sudo tee -a /etc/apt/sources.list.d/grafana.list
```


☑️ Atualize a lista de pacotes
```
sudo apt-get update
```


☑️ Para instalar a versão OSS
```
sudo apt-get install grafana
```


☑️ Versão Enterprise
```
sudo apt-get install grafana-enterprise
```


☑️ Verifique se o Grafana está ativo
```
sudo systemctl status grafana-server
```


☑️ Inicie o serviço do Grafana
```
sudo systemctl start grafana-server
```





☑️  Acessar a Interface Web do Grafana
```
http://<seu_ip>:3000
```
login padrão Usuário: admin

Senha: admin (você será solicitado a alterá-la na primeira vez que acessar).

Acesse o Grafana

1️⃣ Abra seu navegador e faça login na sua instância do Grafana.



2️⃣ Adicionar uma Fonte de Dados

No menu lateral, clique em Configuration (o ícone de engrenagem).

Selecione Data Sources.

Clique em Add data source.



3️⃣ Escolha a Fonte de Dados

Selecione o tipo de fonte de dados que você deseja adicionar (por exemplo, AWS CloudWatch, Prometheus, etc.).



4️⃣ Configurar as Credenciais

Na página de configuração da fonte de dados, você deverá encontrar campos para Access Key, Secret Key e Região. Os campos podem variar dependendo do tipo de fonte de dados que você selecionou, mas geralmente você encontrará algo como:



 Access Key: Insira sua Access Key aqui.

 Secret Key: Insira sua Secret Key aqui.

 Region: Insira a região apropriada (por exemplo, us-east-1, eu-west-1, etc.).



5️⃣ Salvar Configurações

Após inserir as informações, clique em Save & Test para garantir que a configuração está correta e que o Grafana pode se conectar ao serviço.



☑️ Successfully queried the CloudWatch metrics API. 2. Successfully queried the CloudWatch logs API.

Next, you can start to visualize data by building a dashboard, or by querying data in the Explore view.



6️⃣ Uso nas Consultas

Agora você pode usar essa fonte de dados em seus painéis e consultas.



"Nota1

Não compartilhe suas chaves: Certifique-se de que suas chaves não sejam expostas em público.

Use IAM Roles: Se estiver usando AWS, considere usar IAM Roles em vez de chaves diretamente, especialmente em ambientes de produção.



se essa atividade ajudou,não esqueça de curtir e deixe o um comentário.



@heberton geovane

## EC2 

![gr20](https://github.com/user-attachments/assets/2aef152a-e2db-4601-8abe-5e615c3678f4)


## Welcome to Grafana login 

![gr2](https://github.com/user-attachments/assets/f173a4cd-7667-4c55-ae02-ba8e3a67fa13)


## Welcome to Grafana

![gr3](https://github.com/user-attachments/assets/6cadfcbb-0ae2-46a4-b565-a02c63c847ae)

## Grafana CloudWatch 

![gr4](https://github.com/user-attachments/assets/8f04b2f1-c6ef-4a5f-94b8-00048af27080)

## AWS EC2 Região 

![gr5](https://github.com/user-attachments/assets/94761a9b-ca24-44f1-a8ae-d5f4f4000b76)

## Access Key Secret key Região AWS 

![gr6](https://github.com/user-attachments/assets/bc280b23-573f-43fb-84d4-873ba1f1b250)


## Successfull Data Source Save & Test 

![gr8](https://github.com/user-attachments/assets/a88e6bdd-ee55-4209-9b35-043180de91ca)

## Dashboards Create 

![gr9](https://github.com/user-attachments/assets/5f6c8328-d08f-42dc-87a7-b301d6c629e4)

## New 
![gr28](https://github.com/user-attachments/assets/b067a8eb-87ca-4d52-ac91-c8223e6d5007)

## Home Dashborads New Dashboards 

### Time Series 
![gr21](https://github.com/user-attachments/assets/32281e12-0ae1-4e6d-ac4a-221d53a34445)

### Bart Chart 
![gr22](https://github.com/user-attachments/assets/b1d446d6-6a22-4a63-9514-8a899f90ecd6)

### Stat 
![gr23](https://github.com/user-attachments/assets/9d967be3-6161-416a-9834-83e0b63cdf5b)

### Gauge 
![gr24](https://github.com/user-attachments/assets/b04c513a-1a23-4553-a8b7-72415cd001c9)

### Pie Chart 
![gr25](https://github.com/user-attachments/assets/cc68910c-61d5-474d-b94d-1fdebcd174e7)

### Heatmap 
![gr26](https://github.com/user-attachments/assets/ee5a2d06-80b5-4464-8891-4ed5da814ef6)

## Home Dashborads AWS EC2 
![gr27](https://github.com/user-attachments/assets/63b2a90c-2152-45e9-93af-f787aa098170)











