pipeline {
    agent any // El pipeline se ejecutará en cualquier agente disponible

    stages {
        stage('Create File') { // Nombre de la etapa
            steps {
                script {
                    // Crear un archivo con contenido
                    sh '''
                        echo "making my first file" > edward.txt
                        echo "File edward.txt has been created successfully!"
                    '''
                }
            }
        }
    }

    post {
        success {
            echo 'Pipeline executed successfully. File created!'
        }
        failure {
            echo 'Pipeline failed. Please check the logs.'
        }
    }
}
