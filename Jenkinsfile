podTemplate(containers: [
    containerTemplate(
        name: 'test', 
        image: 'test', 
        registryUrl '799861587158.dkr.ecr.ap-south-1.amazonaws.com',
        registryCredentialsId 'ecr:ap-south-1:iam_role'
        ),
    containerTemplate(
        name: 'python', 
        image: 'python:latest', 
        command: 'sleep', 
        args: '30d')
  ]) {

    node(POD_LABEL) {
        stage('Get a Maven project') {
            
            container('test') {
                
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
