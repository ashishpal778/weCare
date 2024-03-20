pipeline {
    agent any

  
    environment {
        NVM_DIR = "/var/lib/jenkins/workspace/React by ChatGPT/.nvm"
    }

    stages {

        stage('Set Up Environment') {
            steps {
                script {
                    // Define NVM_DIR with double quotes
                    def NVM_DIR = "/var/lib/jenkins/workspace/React by ChatGPT/.nvm"

                    // Install nvm
                    sh 'curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.1/install.sh | bash'
                    
                    // Source nvm and set default version
                    sh "export NVM_DIR=${NVM_DIR}"
                    sh "source ${NVM_DIR}/nvm.sh"
                    sh 'nvm install stable'
                    sh 'nvm use stable'
                }
            }
        }

        stage('Install Dependencies') {
            steps {
                script {
                    // Print Node.js and npm versions for verification
                    sh 'node -v'
                    sh 'npm -v'

                    // Install project dependencies
                    sh 'npm install'
                }
            }
        }

        stage('Build') {
            steps {
                script {
                    // Print Node.js and npm versions for verification
                    sh 'node -v'
                    sh 'npm -v'
                    
                    // Install project dependencies
                    sh 'npm install'
                }
            }
        }

        // stage('Test') {
        //     steps {
        //         script {
        //             // Run tests
        //             sh 'npm test'
        //         }
        //     }
        // }

        stage('Deploy') {
            steps {
                script {
                    // Example: Deploy to a server
                    // You would replace this with your actual deployment steps
                    sh 'npm run deploy'
                }
            }
        }
    }
}
