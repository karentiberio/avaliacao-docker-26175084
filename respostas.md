# Respostas · Avaliação Prática de Docker · ViaSerra Transportes (Turma C)

Nome:KAREN 
Matrícula:26175084
Usuário do GitHub:karentiberio
Usuário do Docker Hub:karentiberio

Responda com as suas palavras e com o que aconteceu na SUA máquina. Resposta curta e certa vale mais
do que texto longo copiado. Resposta que contradiz o seu próprio Dockerfile vale zero.

## Parte 1 · Dockerfile do portal

1. Qual imagem base você usou e qual o tamanho final da imagem do portal (saída de `docker images`)? 1.27-alpine. 73.6 MB
2. Em qual pasta do container o Nginx procura os arquivos do site? Mostre o comando que você usou para
conferir que o `index.html` está lá dentro. Pasta: /usr/share/nginx/html Comando: docker exec teste-portal ls /usr/share/nginx/html

## Parte 2 · Docker Hub

3. Nome completo da imagem publicada e link público do repositório no Docker Hub. Nome da imagem: karentiberio/viaserra-portal link: https://hub.docker.com/r/karentiberio/viaserra-portal/tags
4. Se você mudar o HTML, quais comandos precisa rodar para que a versão nova chegue ao Docker Hub? docker build -t karentiberio/viaserra-portal:1.0-26175084 ./portal | docker push karentiberio/viaserra-portal:1.0-26175084

## Parte 3 · Página de manutenção

5. Preencha uma linha por defeito encontrado. Defeito inexistente listado aqui desconta pontos.

|#|Instrução|O que estava errado|O que você viu acontecer|Como corrigiu|
|-|-|-|-|-|
|1|||||
|2|||||
|3|||||

6. Qual a diferença entre `-p 7042:80` e `-p 80:7042` no `docker run`? Qual dos dois números é a porta do container?

## Parte 4 · Primeiro docker-compose

7. Escreva os dois comandos `docker run` que fariam o mesmo que o seu `docker-compose.yml`.
8. Qual comando derruba os dois containers de uma vez?

## Verificador

9. Código de conclusão impresso pelo verificador:

```
scripts\\verificar.ps1



Aviso de segurança

Execute apenas scripts confiáveis. Embora os scripts da Internet possam ser úteis, eles podem danificar seu computador.

&#x20;Se você confia nesse script, use o cmdlet Unblock-File para permitir que o script seja executado sem esta mensagem de

aviso. Deseja executar C:\\Users\\26175084\\Downloads\\avaliacao-docker-viaserra\\scripts\\verificar.ps1?

\[N] Não executar  \[R] Executar uma vez  \[U] Suspender  \[?] Ajuda (o padrão é "N"): r

================================================================

&#x20;Verificador · Avaliação Prática de Docker · Turma C

================================================================

&#x20;Matrícula 26175084 · portal 8084 · manutenção 7084



A. Arquivos e Git

\[ OK ] A1 portal/Dockerfile segue os requisitos

\[ OK ] A2 .env fora do Git e .env.example versionado

\[FALHA] A3 4+ commits e remoto no GitHub (encontrados: 2)

&#x20;        -> faça um commit por parte e configure o origin

\[ OK ] A4 imagem karentiberio/viaserra-portal:1.0-26175084 pública no Docker Hub



B. docker compose

&#x20;        (ainda há lacunas \_\_\_\_ no docker-compose.yml)

\[FALHA] B1 serviços portal e manutencao em execução

&#x20;        -> rode docker compose up -d e confira com docker compose ps

\[FALHA] B2 portal roda a imagem publicada

&#x20;        -> imagem em uso:

\[FALHA] B3 portas: portal em 8084 e manutenção em 7084

&#x20;        -> portal= manutencao=



C. Conteúdo

\[ OK ] C1 portal mostra seu nome e sua matrícula

\[FALHA] C2 página de manutenção servindo o aviso "Voltamos em breve"

&#x20;        -> o container responde, mas não com a página de manutenção (ou não responde)



================================================================

&#x20;Resultado: 4/9 verificações

&#x20;Ainda há falhas. Corrija e rode de novo.

================================================================

PS C:\\Users\\26175084\\Downloads\\avaliacao-docker-viaserra>
```

