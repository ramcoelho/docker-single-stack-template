A comunicação entre o cliente e o proxy reverso se dá via SSL (HTTPS) utilizando um certificado Let's Encrypt. Este diretório guarda os arquivos necessários para realizar esta comunicação.

O script cria-dhpem deve ser executado sempre que você criar uma nova stack. Ele gerará o arquivo contendo a chave Diffie-Hellman do servidor: dhparam.pem

