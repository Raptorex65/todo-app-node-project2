pipeline {
    agent{
      docker{
        image 'node:12-alpine'
                }
            }
    stages {
        stage("Run app on Docker"){
            steps{
                withEnv(["HOME=${env.WORKSPACE}"]) {
                    sh 'yarn install --production'
                    sh 'npm install'
                }   
            }
        }
    }
}
