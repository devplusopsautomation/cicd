podTemplate(containers: [
    containerTemplate(
        name: 'maven', 
        image: 'mavenkljkjkljkljlk:3.8.1-jdk-8', 
        command: 'sleep', 
        args: '30d'
        ),
    containerTemplate(
        name: 'python', 
        image: 'python8098ijpoipoipo:latest', 
        command: 'sleep', 
        args: '30d')
  ]) {

    node(POD_LABEL) {
        stage('Get a Maven project') {
            
            container('maven') {
                
                    sh '''
                    echo "maven build"
                    '''
                
            }
        }
        
        stage('Get a Python Project') {
            
            container('python') {
                
                    sh '''
                    echo "python build"
                    '''
                
            }
        }

        

    }
}
