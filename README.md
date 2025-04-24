# Project Title

Dockerfile Generator

## Description

A GenAI powered tool that generates optimized Dockerfiles based on programming language input. This project uses Ollama with the Llama3 model to create Dockerfiles following best practices.

## Getting Started

1. Initialize the project (Go to any local folder and launch powershell or cmd):
uv init generate-dockerfile
cd generate-dockerfile

3. Create virtual environment and activate it
uv venv
.venv\Scripts\activate


### Dependencies

1. Download and Install Ollama
 For Linux
 curl -fsSL https://ollama.com/install.sh | sh

 For MacOS
 brew install ollama

2. Start Ollama Service

 ollama serve

3. Pull Llama3 Model

 ollama pull llama3.2:latest 

4. Check ollama installed list

 ollama list  

### Installing

1. Create and install requirements.txt

 uv add -r requirements.txt

### Executing program

 * Run the program and update language to publish the outpu
 ```
 uv run main.py
 ```

## Output

 (generate-dockerfile) C:\AI Agent\generate-dockerfile>uv run main.py
 Enter the programming language: java

 Generated Dockerfile:

 ```dockerfile
 Use official Java 8 image as base
 FROM openjdk:8-jdk-alpine

 Set working directory to /app
 WORKDIR /app

 Copy Maven configuration file (if using Maven)
 COPY pom.xml /app/

 Install dependencies
 RUN mvn dependency:resolve -Dmaven.test.skip=true

 Add source code
 COPY . /app/

 Compile and package the application
 RUN mvn clean package

 Run the application
 CMD ["mvn", "run", "-Djvm.options=-Xmx1024m"]
 ```

 Run the application
 CMD ["mvn", "run", "-Djvm.options=-Xmx1024m"]
 ```

 Note: This Dockerfile uses Maven for dependency management. If you're using a different build tool, adjust the commands accordingly.

## Push the code to Github

 echo "# Devops-LLM" >> README.md
 git init
 git add README.md
 git commit -m "first commit"
 git branch -M main
 git remote add origin https://github.com/amana-nkit/Devops-LLM.git
 git push -u origin main

## Help

 Any advise for common problems or issues.
 ```
 command to run if program contains helper info
 ```

## Authors

 Contributors names and contact info

 Aman Ankit

## Version History

* 0.1
    * Initial Release

## License

This project is licensed under the [NAME HERE] License - see the LICENSE.md file for details

## Acknowledgments

Inspiration, code snippets, etc.
* [MCP-CRASH-Course](https://github.com/krishnaik06/MCP-CRASH-Course.git)
* [ai-assisted-devops](https://github.com/iam-veeramalla/ai-assisted-devops.git
