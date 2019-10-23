node('maven'){
    agent none
    stages{
        stage('checkout'){
            steps{
                git 'https://github.com/MAYUR2130/SpringBootNew.git'
            }
        }
        stage('build'){
            steps{
                  sh 'mvn clean install'
            }
        }
        stage('Docker build'){
            steps{
                sh 'docker build -t mayur21/springboot:latest .'
            }
        }
        stage('Docker push'){
            steps{
                withCredentials([string(credentialsId: 'docker_pass', variable: 'dockerPass')]) {
                    sh "docker login -u mayur21 -p ${dockerPass}"
                    }
                
                sh 'docker push mayur21/springboot:latest'
            }
        }
    }   
}
