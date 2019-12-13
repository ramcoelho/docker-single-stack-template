Este diretório aponta para o diretório público do projeto associado ao domínio.

Ele existe apenas para eliminar a necessidade de criar mais uma configuração. Basta criar um link com o nome do domínio apontando para o diretório público do projeto, que está em src/dominio.

Se o seu projeto possui um diretório público (www, wwwroot, htmlroot, public, ou algo parecido), aponte o link para este diretório. Mas se você estiver abrigando uma instalação Wordpress ou similar, em que o diretório raiz é público, aponte diretamente para a raiz:

Ex.:

# Com diretório público:
ln -s ../src/dominio.com.br/public dominio.com.br

# Diretamente na raiz:
ln -s ../src/wordpress.dominio.com.br 


