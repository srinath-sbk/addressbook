pipeline {
    agent any

    tools {
        // Install the Maven version configured as "M3" and add it to the path.
        maven "mymaven"
    }

    parameters{


        string(name: 'ENV', defaultValue: 'Test', description: 'version to deploy')
        booleanParam(name: 'executeTest', defaultValue: true, description: 'decide to run tc')
        choice(name: 'APPVERSION', choices: ['1.1', '1.2', '1.3'])
    }

    stages {
        stage('Compile') {
            steps {
               echo "compiling the code ${params.APPVERSION}"
            }
        }
        stage('UnitTest') {
            steps {
               echo "Test the code $"
            }
        }
        stage('Package') {
            steps {
               echo "Package the code ${params.ENV}"
            }
        }
    }
}
