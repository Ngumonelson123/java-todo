pipeline{
    agent any
    tools{
        gradle "gradle"
    }
    stages{
        stage("Clone Repo"){
            steps{
                git branch: 'master', url: 'https://github.com/Ngumonelson123/java-todo.git'
            }
        }
        stage("Test"){
            steps{
                sh "gradle test"
            }
        }
        
    }
}