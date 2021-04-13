pipeline {
   agent any

   stages {
      stage('Moved to CPMA branch') {
         steps {
           sh '''
           cd /var/lib/jenkins/jobs/CPMA_R3.95.4/workspace/WCBD/dist/server/
           ls -lrt
           '''
         }
      }
      stage('DEV2 S3 Bucket list') {
         steps {
           sh 'aws s3 ls s3://arcadia-wcs-private/artifacts/wcs/TST1/'
        }
      }
   }
}
