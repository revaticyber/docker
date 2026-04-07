pipeline{
 agent any
   stages{
    stage('#1.Checkout'){
     steps{
        git url:'https://github.com/JanhaviThiru/jenrepo.git',branch:'main'
}
}

  stage('#2.Build the image'){
     steps{
     bat 'docker build -t mywebsite.'
}
}
  stage('#3.stop all old containers'){
     steps{
      bat 'docker stop mycont || exit 0'
      bat 'docker rm mycont || exit 0'
}
}

 stage('#4.run teh image - containerise'){
     steps{
      bat 'docker run -d -p 4000:00 --name mycont mywebsite'
}
}
   }
}

 
