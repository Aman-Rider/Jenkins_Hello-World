node {
    stage('Build') {
            echo "Entered Build Stage"
            checkout scm
            sh 'python Simple.py'
            def sonar.projectKey=Jenkins
            def sonar.projectName=Jenkins
            def sonar.projectVersion=1.0
            def sonar.login=admin
            def sonar.password=admin
            def sonar.language=python
            def sonar.sourceEncoding=UTF-8
            def scannerHome = tool 'SonarQube3'
            withSonarQubeEnv('SonarQube') {
                sh "${scannerHome}/bin/sonar-scanner"
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
