node {
    stage('Build') {
        steps {
            echo "Entered Build Stage"
            sh 'python Simple.py
        }
    }
    stage('Test') {
        steps {

        }
    }
    stage('Deliver') {
        steps {
            sh 'pyinstaller --onefile sources/add2vals.py'
        }
    }
}
