node ('slave') {
    stage ('pre-build'){git changelog: false, poll: false, url: 'https://github.com/navila-va/htmlnew.git'
    

    }
    stage ('build'){
        
    
    sh 'sudo service apache2 stop'
    sh 'echo "<html><body><h1>This is a Heading</h1> </body> </html>" >index.html'
    sh 'echo "<body><h1>My First Heading</h1><p>My first paragraph.</p></body></html>" >>index.html'
    sh 'sudo mv index.html /var/www/html/index.html'
    sh 'sudo service apache2 start'

   
    }
    stage ('test'){
        sh 'x=$(curl http://18.224.146.96/index.html)'
        sh 'echo $x'
        
        
    }
    stage ('production'){
    }
  
}
