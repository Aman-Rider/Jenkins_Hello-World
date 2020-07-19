node {
    stage('Build') {
            echo "Entered Build Stage"
            checkout scm
            sh 'python Simple.py'
            SonarQube {
            sh "./Simple.py clean sonarqube"
        }
    }
    stage('Test') {
            echo "Entered Test Stage"
            sh 'python Simple.py'
    }
    stage('Deliver') {
            echo "Entered Deliver Stage"
    }
}
