pipeline {
    agent any
    stages {
        stage('GIt checkout')
        {
            steps {
                echo "checking out"
                //git credentialsId: 'cb38e594-ad9f-4a2b-977b-b6df60645f43', url: 'https://github.com/arajalingam/MyApp3.git'
                git credentialsId: '2d81da45-7142-432e-b00b-9b49c0c759cc', url: 'git@github.com:arajalingam/MyApp3.git'
            }
        }

           stage('build')
        {
            steps {
                echo "build success"
               bat 'build.bat'
            }
        }

   stage('unitestcase')
        {
            steps {
                echo "unit test success"
               bat 'unitestcase.bat'
            }
        }
        stage('quality check')
        {
            steps {
                echo "QC success"
               bat 'qualitycheck.bat'
            }
        }
         stage('deploy')
        {
            steps {
                echo "deploy success"
               bat 'deploy.bat'
            }
        }
    }
}
