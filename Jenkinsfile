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
        stage('Deploy to Heroku') {
  steps {
    withCredentials([usernameColonPassword(credentialsId: '2916c886-aef8-4bc8-95a4-748cb1b5086a', variable: 'HEROKU_CREDENTIALS' )]){
      sh 'git push https://${HEROKU_CREDENTIALS}@git.heroku.com/devops-test.git master'
    }
  }
} 
        
    }
}