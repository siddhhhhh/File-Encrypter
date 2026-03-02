node {

    try {

        stage('Build') {
            sh '''
            cd "Password Protection"
            mkdir -p build
            javac -d build src/*.java
            echo "Build successful"
            '''
        }

        stage('Deploy') {
            sh '''
            cd "Password Protection"
            jar cf FileEncrypter.jar -C build .
            echo "Deployment successful"
            '''
        }

        echo "Pipeline executed successfully!"

    } catch (Exception e) {

        echo "Pipeline failed!"
        throw e
    }
}
