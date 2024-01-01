# docker-cli

## Comandos Básicos:

1. **`docker version`**
   - Exibe a versão do Docker instalada no sistema.

2. **`docker info`**
   - Fornece informações detalhadas sobre o ambiente Docker.

3. **`docker run`**
   - Executa um contêiner a partir de uma imagem.

4. **`docker ps`**
   - Lista os contêineres em execução.

5. **`docker ps -a`**
   - Lista todos os contêineres, incluindo os que estão parados.

6. **`docker --help`**
   - Exibe a ajuda geral para o Docker CLI.

## Gerenciamento de Contêineres:

7. **`docker container ls`**
   - Lista os contêineres em execução.

8. **`docker container ls -a`**
   - Lista todos os contêineres, incluindo os que estão parados.

9. **`docker container ls -a -q`**
    - Retorna apenas os IDs dos contêineres, sem informações adicionais.

10. **`docker container stop [ID]`**
    - Para a execução de um contêiner específico.

11. **`docker container start [ID]`**
    - Inicia um contêiner específico.

12. **`docker container rm [ID]`**
    - Remove um contêiner específico.

13. **`docker container rm -f [ID]`**
    - Remove forçadamente um contêiner específico.

14. **`docker container rm $(docker container ls -a -q)`**
    - Remove todos os contêineres.

## Executando Contêineres com Aplicações Web:

15. **`docker container run -d -P nginx`**
    - Executa o contêiner "nginx" em segundo plano (-d) e mapeia automaticamente as portas (-P).

16. **`docker container run -d -p 8080:80 nginx`**
    - Executa o contêiner "nginx" em segundo plano, mapeando a porta 8080 do host para a porta 80 do contêiner.

17. **`docker container run -d -p 8081:80 nginx`**
    - Executa outro contêiner "nginx", mapeando a porta 8081 do host para a porta 80 do contêiner.

18. **`docker container run -d -p 80:80 --name webhost nginx`**
    - Executa o contêiner "nginx" com um nome específico ("webhost") e mapeia a porta 80 do host para a porta 80 do contêiner.

19. **`docker container run -d -p 81:80 --name webhost2 httpd`**
    - Executa um contêiner "httpd" com o nome "webhost2" e mapeia a porta 81 do host para a porta 80 do contêiner.

## Comandos Adicionais:

20. **`docker container logs [nome/ID]`**
    - Exibe os logs de um contêiner específico.

21. **`docker container top [nome/ID]`**
    - Exibe os processos em execução em um contêiner.

22. **`docker container stats [nome/ID]`**
    - Exibe estatísticas de uso de recursos de um contêiner.

23. **`docker container inspect [nome/ID]`**
    - Exibe informações detalhadas sobre um contêiner.

24. **`docker container inspect -f "{{.NetworkSettings}}" [nome/ID]`**
    - Exibe informações específicas sobre as configurações de rede de um contêiner.

25. **`docker container stop $(docker container ls -a -q)`**
    - Para todos os contêineres em execução.

26. **`docker container rm $(docker container ls -a -q)`**
    - Remove todos os contêineres parados.
