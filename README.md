# maven-java-question-1

comment in simple/>
mvn clean test

git init
git add .
git commit -m "Initial Maven project with JUnit test"
git branch -M main
git remote add origin <your-repository-url>
git push -u origin main

**pipline script**
pipeline {
 agent any
 tools {
 maven 'Maven'
 }
 stages {
 stage('Checkout Git') {
 steps {
 git branch: 'main',
 url: 'https://github.com/prakashumapathi07-spec/maven.git'
 }
 }
 stage('Build and Test') {
 steps {
 bat 'mvn clean test'
 }
 }
 }
}
