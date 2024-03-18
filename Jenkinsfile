pipline{

    agents any

    parameters{
        
        string(name: 'Version', defaultValue: '', description: 'Version to deploy on prod')
        booleanParam(name: 'ExecuteTests', defaultValue: true, description: '')
    }

    stages{
        stage("Build"){
            steps{
                echo 'Building'
            }   
        }

        stage("Testing"){
            steps{
                when{
                    expression{
                        params.booleanParam
                    }
                }
                echo 'Testing...'
            }
        }

        stages("Deploy"){
            steps{
                echo 'Deploying.....'
                echo "Deploying version ${params.VERSION}"
            }
        }    
        }
    }
