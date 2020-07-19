node {
    stage('Build') {
            echo "Entered Build Stage"
            checkout scm
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
