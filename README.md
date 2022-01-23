# terraform
Utilizando Terraform e Cluster Kubernetes com o provider Azure

- Instalar a extensao na IDE do vscode hashicorp terraform para auxiliar na escrita do código
- Instalar o CLI do provider que você estara utilizando

Sempre quando adicionar um novo provider utilizar o comando abaixo:
terraform init

Verificar a estrutura do codigo e dar sequencia nos passos a serem seguidos:
terraform plan

observação: realizar o login na azure com o comando az login (ou provider que estiver utilizando)

Para aplicar o plano que foi realizado:
terraform apply

Checar as vms disponiveis na sua região:
az vm list-sizes --location brazilsouth -o table

Conectar ao kubernetes:
az aks get-credentials --resource-group vm-david --name vm-david-kubernetes

Verificar os nodes:
kubectl get nodes

Aplicar diretamente o plano sem necessidade de aprovação manual:
terraform apply --auto-approve

Finalizar a estrutura, deletando as vms e os nós que estam rodando no provider:
terraform destroy
