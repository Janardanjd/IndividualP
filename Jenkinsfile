/* groovylint-disable CompileStatic */
pipeline {
    agent any
    parameters {
        choice (name: 'VERSION' , choice: ['1.0.0', '1.1.0', '1.2.0'], desciption: '' )
        booleanParam( name: 'executeTest', defaultValue: true, description: '')
    }
    stages {
        stage ("build"){
            steps {
                echo 'build project is started....done'
            }
        }
        stage("Test") {
            when {
                expression {
                    parameters.executeTest
                }
            }
            steps {
                echo 'testinh testing the appliaction is started....done'

            }
        }
        stage ("deploy") {
            steps {
                echo 'deplying the application started....done'
                echo "deploying the version ${parameters.VERSION}"
            }
        }

        }
}
