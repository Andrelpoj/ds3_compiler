# DS3 Checker

Model Checker para a lógica DS3.

## Manual para Instalação e Execução}  

É necessário possuir o Docker instalado, as outras dependências são tratadas pelo próprio container.

Para executar o DS3 Checker no container Docker, basta seguir os passos:


1. Navegar até a pasta do projeto clonado do github
2. Construir a imagem Docker
    ```  docker build ./ -t ds3checker --rm ```
3. Navegar até a pasta onde estão os modelos e arquivos do seu projeto
4. Iniciar a execução do container (o comando abaixo realiza o espelhamento entre a pasta atual e a pasta workspace no container)
    ``` docker run -it --rm -v "$(pwd)/:/workspace" ds3checker ```
5. Ativar o ambiente python correto dentro do container
    ``` source /opt/venv/bin/activate ```

6. Realizar chamadas ao DS_3 Checker com os seguintes parâmetros:
  - A fórmula para ser verificada utilizando a sintaxe da linguagem do DS3 Checker. 
  - A SPN, que será utilizada para construir o modelo e verificar a fórmula, codificada em PNPRO.
 
