#!groovy
pipeline{
    agent any
    stages {
        stage ("Build"){
            steps{
                echo 'Building'
                
            }
        }
        stage ("Test"){
            steps{
                bat '''
                pip install python-jenkins
                python -m pip install --upgrade pip
                pip install virtualenv
                virtualenv env
                env//s//activate
                '''
                bat '''
                cd submarino
                python -m Pyautomators -f json -o .//hello-submarino.json
                '''
   
            }
        }
    }
}
