pipeline {
   agent any
   stages {
        stage('Checkout') {
            steps {
                checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[credentialsId: 'GitHub_Cred', url: 'https://github.com/Pranesh-poojary/ShoppingCart.git']]])
                sh "ls -lart ./*"
            }
        }
      stage('maven build') {
            steps {
                bat "mvn clean package"
            }
       }
   }
}
