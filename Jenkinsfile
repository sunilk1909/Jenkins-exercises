pipeline {
    agent any
       environment {
            // GIT_CREDENTIALS_ID = 'your-credentials-id' // Replace with your Jenkins credentials ID
        }

    stages {
        stage('Increment version') {
             script {
                                def version = readFile('package.json').trim()
                                def parts = version.tokenize('.').collect { it as int }

                                if (params.versionLevel == 'major') {
                                    parts[0] += 1
                                    parts[1] = 0
                                    parts[2] = 0
                                } else if (params.versionLevel == 'minor') {
                                    parts[1] += 1
                                    parts[2] = 0
                                } else {
                                    parts[2] += 1
                                }

                                def newVersion = "${parts[0]}.${parts[1]}.${parts[2]}"
                                writeFile file: 'version.txt', text: newVersion
                                echo "Version updated to ${newVersion}"


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
