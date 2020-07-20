node {
    stage('Build') {
            echo "Entered Build Stage"
            checkout scm
            sh 'python Simple.py'
            property "sonar.projectKey", "Jenkins" 
            property "sonar.projectName", "Jenkins" 
            property "sonar.login", "admin"
            property "sonar.password", "admin" 
            property "projectVersion", "1.0"
            property "sonar.language", "python" 
            property "sonar.sourceEncoding", "UTF-8"
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
