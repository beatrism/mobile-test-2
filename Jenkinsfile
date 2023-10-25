pipeline {
    agent any


    stages {
        stage('Clonar o repositório') {
            steps {
                git branch: 'main', url: 'https://github.com/beatrism/mobile-test-2.git'
            }
        }

    
        stage('Instalar dependencias') {
             
            steps {
                nodejs('node'){
                    bat 'npm install'
                            }
                    }
        }
    
        stage('Executar Testes') {
            steps {
                 nodejs('node'){
                    bat 'npm run wdio'
                }
                        }
        }
}
    
    
}
