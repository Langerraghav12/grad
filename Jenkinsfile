pipeline{
agent any
tools{
gradle 'Gradle'
jdk 'JDK'
}
stages{
stage('Checkout'){
steps{
git branch: 'main' ,url:'https://github.com/ankitjha100/gradlejenkins.git'
}}
stage('Build'){
steps{
sh 'gradle build'
}}
stage('Test'){
steps{
sh 'gradle test'
}}
stage('Run'){
steps{
sh 'gradle run'
}}}
post{
success{
echo 'Build success'
}
  failure{
echo 'Build failed'
}}}
