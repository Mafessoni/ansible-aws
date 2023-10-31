# ansible-aws

Nesse playbook faço todas as instalações necessárias para rodar o Docker e a AWS CLI.

- Configuro a AWS CLI com aws_access_key e aws_secret_key.
  PS: É necessario informar os dados nas variáveis dentro do arquivo ./vars/main.yaml

- Faço o pull de uma imagem do ECR

- Rodo um container fazendo um port_bindings na porta 4000

# Para rodar o playbook:

Para baixar a imagem latest:

```bash
$ ansible-playbook -i hosts main.yaml
```

Para baixar uma versão especifica da imagem utilize:

```bash
$ ansible-playbook -i hosts main.yaml --extra-vars image_tag=TAG
```
