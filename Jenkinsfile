pipeline{
    agent {
        label 'testNode1'
    }
    // options {
    //     skipDefaultCheckout()
    // }
    stages {
        stage('read config') {
            steps {
                script {
                    config = readYaml file: env.WORKSPACE + '/pipeline_config.yml'
                    echo config
                }
                sh "ls ${env.WORKSPACE}"
            }
        }
        stage('test') {
            steps{
                echo 'config'
            }
        }
    }
}