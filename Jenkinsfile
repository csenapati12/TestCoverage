pipeline {
    agent any

    stages {
        stage('testing1'){
        steps{
        echo "testing"
        }
        }
    }
    post {
        always {
            junit '**/nosetests.xml'
            step([$class: 'CoberturaPublisher', autoUpdateHealth: false, autoUpdateStability: false, coberturaReportFile: '**/coverage.xml', failUnhealthy: false, failUnstable: false, maxNumberOfBuilds: 0, onlyStable: false, sourceEncoding: 'ASCII', zoomCoverageChart: false])
        }
    }
}
