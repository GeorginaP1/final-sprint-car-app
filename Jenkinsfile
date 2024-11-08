pipeline {

    agent any
 
    stages {

        stage('Clone parent folder') {

            steps {

                script {

                    // Clone the third repository

                    git branch: 'main', url: 'https://github.com/GeorginaP1/final-sprint-car-app.git'

                }

            }

        }
 
        stage('Clone and place react front-end ') {

            steps {

                script {

                    // Clone repo1 into a temporary directory

                    dir('frontend_temp') {

                        git branch: 'main', url: 'https://github.com/GeorginaP1/lbg-car-react-starter.git'

                    }

                    // Copy frontend into a subdirectory within the third repository

                    // sh 'cp -r frontend_temp/* frontend/'

                }

            }

        }

        stage('Clone and place spring back-end ') {

            steps {

                script {

                    // Clone backend into a temporary directory

                    dir('backend') {

                        git branch: 'main', url: 'https://github.com/GeorginaP1/lbg-car-spring-app-starter.git'

                    }

                    // Copy backend into a subdirectory within the third repository

                    // sh 'cp -r backend_temp/* backend/'

                }

            }

        }
 
 
        stage('Commit and Push Changes') {

            steps {

                script {

                    // Commit the changes

                    sh 'git add .'

                    sh 'git commit -m "Added frontend and backend contents to respective subdirectories"'
 
                    // Push the changes back to the third repository

                    sh 'git push origin main'

                }

            }

        }

    }

}

 