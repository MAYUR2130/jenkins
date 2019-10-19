pipeline{
    agent any
    stages{
        stage('checkout'){
            steps{
                git 'https://github.com/MAYUR2130/SpringBootNew.git'
            }
        }
        stage('build'){
            steps{
                  sh label: '', script: 'mvn clean install'
            }
        }    
    }   
}
