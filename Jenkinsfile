properties([parameters([choice(choices: ['start', 'stop'], description: 'Select a choice to take action', name: 'choice'), string(defaultValue: '', description: 'Add your Instance Id here', name: 'instaceId', trim: false)])])                
    node {
            if ( "${choice}" == "start" ){
              stage("Start Instance ") {
              
                try{
               
                sh "aws ec2 start-instances --instance-ids ${instaceId}"
                
                }
                catch (Exception e){
                     def stage_name = env.STAGE_NAME
                     def err_msg =  "Failed at stage ${stage_name} . Aws ec2 failed in Starting of instance ${e}"
                        echo "${err_msg}"
                }
               }
              }
            if ( "${choice}" == "stop" ){
            stage("Stop Instance ") {
                
               
                try{
                     sh "aws ec2 stop-instances --instance-ids ${instaceId}
                }
                catch (Exception e){
                     def stage_name = env.STAGE_NAME
                     def err_msg =  "Failed at stage ${stage_name} . Aws ec2 failed in Stoping of instance ${e}"
                     echo "${err_msg}"
                }
              }
              }

            }
