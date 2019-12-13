Este template usa a imagem base para PHP-FPM.

Caso necessário, crie sua própria imagem habilitando módulos ou instalando ferramentas secundárias (como Composer) para usar em seu container.

Veja exemplo no arquivo Dockerfile.

Para criar uma imagem local, execute o comando a seguir no diretório onde está o Dockerfile:

$ docker build -t 'nome-da-imagem' .

No seu docker-compose.yaml, utilize o nome da imagem escolhido para o parâmtro 'image' do container
