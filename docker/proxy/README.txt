O diretório le-challenge-root serve para guardar os arquivos temporários criados pelo script bin/getcert no processo de aquisição de certificados. Este é o único motivo pelo qual o proxy usa a porta 80.

O diretório nginx contém os arquivos de configuração dos clientes desta stack.

Utilize um arquivo .conf para cada cliente, uma seção 'server' para cada domínio dentro deste arquivo e uma seção 'location' dentro de cada 'server' para os contextos de aplicação. Cada aplicação (seja acessível por um hostname específico ou um contexto dentro de um hostname) deve possuir seu próprio container nginx, criado no arquivo docker-compose.yaml.

Dentro de cada seção 'location', você deve definir pelo menos 5 parâmetros:

  - proxy_pass: Indique o container que servirá esta aplicação (Ex.: https://nome-do-container)
  - X-PHP-Container: Indique qual container PHP lidará com o processamento
  - X-Client-Home: Qual diretório de cliente guarda esta aplicação
  - X-Domain: Qual o FQDN desta aplicação (o diretório client/algum-cliente/public deve ter um link com este nome)
  - X-Context: Qual o contexto desta aplicação (root, se estiver na raiz)



