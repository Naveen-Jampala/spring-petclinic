pipeline {
    agent{label 'JAVA'}  //the java is label name inisde jenkins so here also must match
    stages{
        stage('git checkout') {
            steps{
            git url : 'https://github.com/Naveen-Jampala/spring-petclinic.git',
            branch : 'main'
            }
        }
        stage('build & test') {
            steps{
                sh 'mvn package sonar:sonar'
            }
        }
    }
}