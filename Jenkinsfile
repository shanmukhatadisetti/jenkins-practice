pipeline{
    agent {
        label 'agent-1'
    }
    environment{
        course="jenkins"
    }
    options {
                // timeout(time: 10, unit: 'SECONDS') 
                disableConcurrentBuilds()
                retry(3)
    }
    parameters {
        string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')

    }

    stages{
        stage('build'){
            steps{
                script{
                    sh """
                    echo 'building....'
                    sleep 20
                    env
                    echo "${params.PERSON}"
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
             input {
                message "Should we continue?"
                ok "Yes, we should."
                submitter "alice,bob"
                parameters {
                    string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')
                }
            }
            steps{
                script{
                    echo 'deploying ....'
                }

            }
        }
    }
}