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
                    config = readYaml file: env.WORKSPACE + '/demo/config.yaml'
                    echo config
                }
            }
        }
        stage('test') {
            steps{
                echo config
            }
        }
    }
}