pipeline {
    agent any 
    stages {
        stage ("git checkout"){
            steps {
                script {
                    git url:'https://github.com/gunjisreehari16/javaSpringBoot.git', branch:'master'
                }
            }
        }
        stage('Docker build'){
            steps {
                script {
                    sh 'docker build -t gsreehari/javaspringboot:1 .'
                }
            }
        }
        stage('Docker push'){
            steps {
                script {
                    sh 'docker login -u gsreehari -p camp@1122'
                    sh 'docker push gsreehari/javaspringboot:1'
                }
            }
        }
    }
}
