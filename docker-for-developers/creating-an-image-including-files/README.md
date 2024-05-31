docker build -t webserver .
docker run --rm -it -p 8082:80 webserver

Os comandos acima constroem um servidor web a partir das instruções do arquivo Dockerfile e, em seguida, iniciam um
contêiner que escuta a porta 8082 da minha máquina e redireciona as conexões de entrada para a porta 80 do contêiner.
Você pode iniciar um navegador e apontá-lo para http://localhost:8082visualizá-lo localmente. Isso exibe o conteúdo do
arquivo HTML no navegador, pois ele é servido por HTTP pelo contêiner em execução:


A opção -it me permite parar o contêiner usando Ctrl-C na linha de comando

A opção –rm garante que o contêiner seja excluído assim que for interrompido
