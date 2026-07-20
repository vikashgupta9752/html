pipeline
{
    agent any
    stage ('Checkout')
    steps{
        git branch: 'main'
        url:'https://github.com/vikashgupta9752/html.git'

    }
    stage ('Test')
    steps{
        sh 'test -f index.html'
        echo 'Application file index.html found'
    }
    // stage('Deploy')
    // steps{
    //     sh ''' mkdir -p /var/www/html
    //     cp -r * /var/www/html
    //     '''
    // }
    post{
        success{
            echo 'Pipeline executed successfully'
        }
        failure{
            echo 'Pipeline execution failed'
        }
    }
}