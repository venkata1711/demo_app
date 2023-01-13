pipeline {
     agent any

     stages{

        stage('Git Checkout'){

            steps{
                git branch: 'main', url: 'https://github.com/venkata1711/demo_app.git'
            }
        }
     
        stage('Unit Testing'){
           
             steps{
               
                bat 'mvn test'
            }
        }

        stage('Integration Testing'){

            steps{

                bat 'mvn verify -DskipUnitTests'
            }
        }

        stage('Maven Build'){

            steps{

                bat 'mvn clean install'
            }
        }

     }
}
