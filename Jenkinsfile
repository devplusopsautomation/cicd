podTemplate(containers: [
    containerTemplate(
        name: 'maven', 
        image: 'mavenjejkwhefjkwhefkjw:3.8.1-jdk-8', 
        command: 'sleep', 
        args: '30d'
        ),
    containerTemplate(
        name: 'python', 
        image: 'pythondkejdklwjdklwejdklwejdwelk:latest', 
        command: 'sleep', 
        args: '30d')
  ]) {

    node(POD_LABEL) {
        stage('Get a Maven project') {
            
            container('maven') {
                stage('Build a Maven project') {
                    sh '''
                    echo "maven build"
                    '''
                }
            }
        }

        stage('Get a Python Project') {
            
            container('python') {
                stage('Build a Go project') {
                    sh '''
                    echo "Go Build"
                    '''
                }
            }
        }

    }
}
