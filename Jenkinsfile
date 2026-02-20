pipeline{
    agent {
        label 'agent-1'
    }
    environment{
        course="jenkins"
    }
    options {
                timeout(time: 10, unit: 'SECONDS') 
                disableConcurrentBuilds() 
            }
    stages{
        stage('build'){
            steps{
                script{
                    sh """
                    echo 'building....'
                    sleep 20
                    env
                    """

                }
            }
        }
        stage('test'){
            steps{
                script{
                    echo 'testing....'
                }

            }
        }
        stage('deploy'){
            steps{
                script{
                    echo 'deploying ....'
                }

            }
        }
    }
}