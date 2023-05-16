pipeline{
    agent any
    stages{
        stage("Stage1 : checkout stage "){
            steps{
                git branch: 'main', url: 'https://github.com/anurocky/mvnproject.git'
               
            }
        }
        stage("Stage2 : compile the code"){
            steps{
                sh "mvn compile"
            }
        }
        stage("Stage3 : uni test"){
            steps{
                sh "mvn test"
            }
        }
        stage("Stage4 : QA"){
            steps{
                sh "mvn pmd:pmd"
            }
        }
        stage("Stage5 : package"){
            steps{
                sh "mvn package"
            }
        }
    }
}
