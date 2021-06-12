# Ansible lab #

Repositório com alguns playbooks voltados a configuração de serviços em Linux.


## Contribuidores
- [Sayonara Santos](https://github.com/sayonarasantos)


## Configurações testadas
- Ansible: 2.9
- S.O.: Ubuntu 20.04
- Python: 2.7


## Lista de playbooks
- `configure_new_remote_user.yaml`: criação de usuário remoto, mudança de posse de arquivos e adição de chave SSH pública para esse usuário


## Como utilizar
### Pre-requisitos
- O pacote do Ansible instalado na máquina gerenciadora;
- O pacote Python instalado nas máquinas gerenciadas e na gerenciadora;
- O acesso SSH configurado (o acesso da máquina gerenciadora às gerenciadas)


### Execução
1. Crie um inventário como o modelo do diretório `inventory_model`;
```
cp inventory_model inventory -R
```

2. E execute o comando:
```
ansible-playbook <caminho do playbook> --private-key <caminho da chave privada para acesso do Ansible> -i <caminho do hosts.ini>
```