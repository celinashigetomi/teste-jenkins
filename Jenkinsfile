// Define o pipeline (o conjunto de instruções)
pipeline {
    // 'agent any' significa que o Jenkins pode rodar estes passos em qualquer máquina disponível
    agent any

    // 'stages' divide o trabalho em etapas lógicas
    stages {
        // A primeira (e única) etapa do nosso pipeline
        stage('Ler o arquivo de dados') {
            // 'steps' são as ações a serem executadas nesta etapa
            steps {
                // Usamos um bloco 'script' para poder usar programação mais livre
                script {
                    // O comando 'readFile' lê o conteúdo do arquivo especificado
                    def conteudoDoArquivo = readFile 'dados.txt'

                    // O comando 'echo' imprime uma mensagem no log do Jenkins
                    echo "========= INÍCIO DO ARQUIVO =========="
                    echo "O conteúdo do arquivo é: \n${conteudoDoArquivo}"
                    echo "========== FIM DO ARQUIVO ==========="
                }
            }
        }
    }
}