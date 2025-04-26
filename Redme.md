### Construindo a Imagem Docker

1.  Clone este repositório (se aplicável) ou crie um diretório com o arquivo `Dockerfile` dentro.

2.  Abra um terminal e navegue até o diretório onde o `Dockerfile` está localizado.

3.  Execute o seguinte comando para construir a imagem Docker:

    ```bash
    docker build -t meu-mongodb .
    ```

    * `docker build`: Comando para construir uma imagem Docker.
    * `-t meu-mongodb`: Define um nome (`tag`) para a sua imagem como `meu-mongodb`. Você pode substituir `meu-mongodb` pelo nome que preferir.
    * `.`: Indica que o `Dockerfile` está no diretório atual.

### Executando o Contêiner MongoDB

Após a construção da imagem, você pode executar um contêiner a partir dela com o seguinte comando:

```bash
docker run -d -p 27017:27017 --name mongodb-container meu-mongodb