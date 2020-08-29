node {
    agent { docker { image 'python:3.7.2' } }
    stage('Build') {
            echo "Entered Build Stage"
            checkout scm
            sh 'pip install flask'
            sj 'pip freeze'
            sh 'python Simple.py'
            
    }
    stage('Test') {
            echo "Entered Test Stage"
            sh 'python Simple.py'
    }
    stage('Deliver') {
            echo "Entered Deliver Stage"
    }
}
