podTemplate(containers: [
    containerTemplate(
        name: 'test', 
        image: 'test:latest', 
        registryUrl: '799861587158.dkr.ecr.ap-south-1.amazonaws.com',
        registryCredentialsId: 'ecr:ap-south-1:iam_role'
        ),
    containerTemplate(
        name: 'python', 
        image: 'python:latest', 
        command: 'sleep', 
        args: '30d')
  ]) {

    node(POD_LABEL) {
        stage('terraform init') {
            
            container('test') {
                
                    sh '''
                    echo "terraform init"
                    '''
                
            }
        }
        
        stage('terraform apply') {
            
            container('python') {
                
                    sh '''
                    echo "terraform apply"
                    '''
                
            }
        }

        

    }
}
