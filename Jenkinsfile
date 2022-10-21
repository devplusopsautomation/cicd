
podTemplate(containers: [
    containerTemplate(
        name: 'test', 
        image: '799861587158.dkr.ecr.ap-south-1.amazonaws.com/bms:test', 
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

