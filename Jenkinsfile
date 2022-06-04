node {
    def mvnHome
    stage('initial_clean_up') {
        cleanWs()
    }
    stage('git_code_pull') {
        git url: 'https://github.com/arghaya/locus-assignment1.git', branch: 'main', credentialsId: '28e81a92-ece2-4b34-bfcf-edbbd30d6f3c'
    }
    stage('Build') {
        sh 'ls'
    }
    stage('Results') {
        sh 'pwd'
    }
    stage('postbuild_clean_up') {
        cleanWs()
    }
    stage('Build Deploy Code') {
            when {
                branch 'develop'
            }
            steps {
                sh """
                echo "Building Artifact"
                """

                sh """
                echo "Deploying Code"
                """
            }
    }
}
