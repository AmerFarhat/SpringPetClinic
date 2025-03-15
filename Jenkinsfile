pipeline{
    agent any
    tools {maven "Amer"}
    stages{
        stage("checkout"){
            steps{
                git branch: "main", url: "https://github.com/AmerFarhat/SpringPetClinic.git"
            }
        }
        stage("build"){
            steps{
                sh "mvn compile"
            }
        }
        stage("test"){
            steps{
                sh "mvn test"
            }
        }
        stage("package"){
            steps{
                sh "mvn package"
            }
        }
        stage("deploy"){
            steps{
                sh "Java -jar ./target/*.jar"
            }
            
        }
    }
}
