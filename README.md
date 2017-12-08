# Enviroment Magento

## Recursos instalados

- PHP 7.1 (FPM)
- Nginx

## Como utilizar

1. Colocar seus arquivos da loja (ou criar um link simbólico de onde estão na sua máquina) para a pasta `magento`.
2. Configurar seu domínio nos arquivos `env/magento.conf` na *linha 4* e no arquivo `docker-compose.yml` na *linha 17*.
3. Alterar seu arquivo de hosts incluindo o host para seu domínio, Ex: `127.0.0.1 seuteste.sualoja`.
4. Configurar a conexão do banco de dados para conectar no `magenv-db:3306`, usuário e senha: `magento`.

### Comandos úteis

Subir os containers:

`docker-compose up -d`

Visualizar logs de um container específico:

`docker-compose logs -f <nome do container>`

## Avisos importantes

- As permissões dos seus diretórios devem estar corretas.
- Caso não consiga acesso ao banco de dados, você deve adicionar as permissões corretas ao usuário (GRANT PRIVILEGES ...).