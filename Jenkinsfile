pipeline {
    agent any

    stages {
        // Etapa para validar o arquivo
        stage('Validar o Arquivo') {
            steps {
                script {
                    sh 'echo "Validar o Arquivo"'
                }
            }
        }

        // Etapa para ler o conteúdo do arquivo
        stage('Ler o Arquivo de Dados') {
            steps {
                script {
                    // O comando 'readFile' lê o conteúdo do arquivo especificado
                    def conteudoDoArquivo = readFile 'teste-carga.xml'

                    // O comando 'echo' imprime uma mensagem no log do Jenkins
                    echo "========= INÍCIO DO ARQUIVO =========="
                    echo "O conteúdo do arquivo é: \n${conteudoDoArquivo}"
                    echo "========== FIM DO ARQUIVO ==========="
                }
            }
        }

        // Etapa de compilar o código (exemplo usando Maven)
        stage('Compilar o Código') {
            steps {
                script {
                    sh 'echo "Compilar o Código"'
                }
            }
        }

        // Etapa para executar testes (exemplo com Maven)
        stage('Executar Testes') {
            steps {
                script {
                    sh 'echo "Executar Testes"'
                }
            }
        }

        // Etapa para empacotar o projeto
        stage('Empacotar o Projeto') {
            steps {
                script {
                    sh 'echo "Empacotar o Projeto"'
                }
            }
        }

        // Etapa de deploy (opcional)
        stage('Fazer Deploy') {
            steps {
                script {
                    echo "Realizando o deploy do pacote gerado..."
                    // Exemplo fictício de comando de deploy
                    sh 'echo "Deploy feito com sucesso no ambiente de homologação!"'
                }
            }
        }
    }
}
