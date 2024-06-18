pipeline {
    agent any
    
    stages {
     
    
        
        stage('Setup') {
            steps {
                // Executar o build da aplicação (substitua com o comando apropriado)
                sh 'npm install'  // Exemplo com npm
            }
        }
        
        stage('Test') {
            steps {
                // Executar os testes da aplicação (substitua com o comando apropriado)
                sh 'npm run cy:run'  // Exemplo com npm
            }
        }
        
        stage('Deploy') {
            steps {
                // Implementar a aplicação (substitua com o comando apropriado)
                publishHTML([allowMissing: false, alwaysLinkToLastBuild: false, keepAll: false, reportDir: 'mochawesome-report', reportFiles: 'mochawesome.html', reportName: 'EBAC Report', reportTitles: '', useWrapperFileDirectly: true])
            }
        }
    }
    

}
