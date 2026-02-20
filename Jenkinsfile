pipeline{
    agent {
        label 'agent-1'
    }
    enironment{
        course=jenkins
    }
    stages{
        stage('build'){
            steps{
                script{
                    sh """
                    echo 'building....'
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