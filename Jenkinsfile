def readYaml(yamlFile) {
    def resutl = ""
    result = readYaml file: yamlFile
    result.each{
        println(it.key + "=" + it.value)
    }
}
pipeline{
    agent {
        docker {
            label 'master'
            images 'centos'
        }
    }
    stages {
        stage('read config') {
            steps {
                readYaml('config.yaml')
            }
        }
        stage('test') {
            steps{
                echo 'testing'
            }
        }
    }
}