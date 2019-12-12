Estes arquivos têm o objetivo de simplificar a gestão de certificados Let's Encrypt. 

Por padrão, instalo os arquivos do stack docker em /var/projetos. Caso você utilize um diretório diferente, deve alterar os arquivos, pois os volumes precisam ser montados com caminho absoluto.

O script 'renewcert' deve ter sua execução agendada no cron.

Ex.:

/etc/cron.d/certbot
-------------------
0 */10 * * * root /var/projetos/bin/renewcert
