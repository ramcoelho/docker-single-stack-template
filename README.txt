Este template visa fornecer um ambiente rápido para desenvolvimento de aplicações multi-tier PHP usando Docker

O arquivo docker-compose.yaml inicia o seguinte ambiente com "docker-compose up":

1. Proxy Reverso NGINX
    Você deve configurar este componente em proxy/nginx

2. Servidor NGINX da Aplicação
    Você deve criar um container para cada tier (api, spa, middleware)

3. Banco de dados MySQL
    Dados em mysql/data e scripts em mysql/backup. Se a sua aplicação usa um SGBD diferente, 
    você deve alterar a imagem de acordo

4. PHP-FPM
    Todos os containers de aplicação podem usar o mesmo container PHP-FPM. Caso precise ativar/desativar
    módulos, adicionar ferramentas (composer, node), crie sua própria imagem. Veja exemplo em docker/php/README.txt

Acrescente seus próprios containers conforme a necessidade (redis, workers, ci/cd)

Versionando seu ambiente, você permite que novos desenvolvedores integrem rapidamente o seu time, sem downtime.

Os scripts em instdocker/ instalam docker e docker-compose no seu ambiente de maneira rápida.

