A comunicação entre o proxy reverso e os containers de aplicação se dá via SSL (HTTPS) utilizando um certificado auto-assinado. Este diretório guarda os arquivos necessários para realizar esta comunicação.

O script cria-certificado deve ser executado sempre que você criar uma nova stack. Ele gerará os arquivos necessários para a comunicação entre os servidores NGINX: nginx.key, nginx.crt, dhparam.pem

