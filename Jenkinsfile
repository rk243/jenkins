
pipeline {
    agent {
        label 'AGENT-1'
    }
    options {
        timeout(time: 30, unit: 'MINUTES')
        disableConcurrentBuilds()
    }
    parameters {
        string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')
        text(name: 'BIOGRAPHY', defaultValue: '', description: 'Enter some information about the person')
        booleanParam(name: 'TOGGLE', defaultValue: true, description: 'Toggle this value')
        choice(name: 'CHOICE', choices: ['One', 'Two', 'Three'], description: 'Pick something')
        password(name: 'PASSWORD', defaultValue: 'SECRET', description: 'Enter a password')
    }
    environment {
        DEPLOY_TO = 'Production'
        GREETING = 'Good Morning'
    }
        stages {
            stage ('Build') {
                steps {
                sh "echo this is Build"
                sh 'env'
            }
        }
            stage ('Test') {
                steps {
                sh "echo this is Test"
            }
        }
            stage ('Deploy') {
                steps {
                sh "echo this is Deploy"
            }
        }
            stage ('Print Params') {
                steps {
                    echo "Hello ${params.PERSON}"
                    echo "Biography: ${params.BIOGRAPHY}"
                    echo "Toggle: ${params.TOGGLE}"
                    echo "Choice: ${params.CHOICE}"
                    echo "Password: ${params.PASSWORD}"
                    echo "Triggered Testt"
                }
            }
    }  
    post { 
        always { 
            echo 'I will always say Hello again!'
        }
        success { 
            echo 'I will run when pipeline is sucess'
        }
        failure { 
            echo 'I will run when pipeline is failure'
        }
    }
}