def readYaml(yamlFile) {
    def resutl = ""
    result = readYaml file: yamlFile
    result.each{
        println(it.key + "=" + it.value)
    }
    return result
}
pipeline{
    agent {
        label 'testNode1'
    }
    stages {
        stage('read config') {
            steps {
                script {
                    config = readYaml('config.yaml')
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