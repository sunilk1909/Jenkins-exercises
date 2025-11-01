pipeline {
    agent any
       environment {
            // GIT_CREDENTIALS_ID = 'your-credentials-id' // Replace with your Jenkins credentials ID
        }

    stages {
        stage('Increment version') {
             script {
                       


             /*
             1. Pull the data from github
             2. Increment the version
             3. Create docker image
             3a. Commit the code to git repo
             4. Upload the image to docker private repo
             5. Create new server, ssh into git
             6. Pull the image, install docker and additional dependecies like npm
             7. Run the server with new image
              */

                            }

        }

        stage('Build') {
            steps {
                echo 'Building the project...'
                // Add your build commands here, e.g., compile code
            }
        }

        stage('Test') {
            steps {
                echo 'Running tests...'
                // Add your test commands here, e.g., run unit tests
            }
        }
    }
}
