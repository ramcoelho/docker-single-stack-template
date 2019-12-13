Este diretório guarda arquivos relacionados ao seu banco de dados local MySQL.

Não utilize esta estratégia em produção

Os diretórios serão montados assim no container de banco:

data -> /var/lib/mysql (Arquivos de dados do MySQL, para que o container
                        possa ser recriado sem perder os dados)
backup -> /backup (Para que você possa trocar scripts de backup/restore)

