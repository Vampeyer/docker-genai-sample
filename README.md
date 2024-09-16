

This is a fork from the repository  - https://github.com/craig-osterhout/docker-genai-sample

From the OFFICIAL DOCKER DOCS  , located here  - https://docs.docker.com/guides/use-case/genai-pdf-bot/

- This version is working as of  09/16/2024 - 




------------------------------------

Running the application. 


- To run the aplication properly , your device must meet the following prerequisites. 

 1. Docker running on the machine  
 2 . Neo4j Docker image running , by pulling the official Neo4j image from Docker hub  , and running it on port
      - "7474:7474"
      - "7687:7687"
  -- To see if you have it connected properly , you may visit localhost:7474 to see if it is running , 
      - While it is running in docker container , and you should see a site displaying its content. 
3. Ollama in a Dockerized container must also be running on port 11434. 
  -- To see if you have it connected properly , you may visit localhost:11434 to see if it is running , 
      - While it is running in docker container , and you should see a site displaying its content. 



4. With neo4j and Ollama hooked up and configured properly , after running them in docker , 
  you should be able to run  

docker compose up --build    

and build and run the project from there. 




---------------------------------------------------------------
-----------------------------------------------
-------------------------------
-----------------
-----------
----
-
-



Updates 
_____________________________________________________________________________

- Updated the requirements.txt file  , through a variation of a .venv and retesting. 

- Intialized a dockerfile , using dockerinit ,   selcting the following variations. 
		- Python 	
		- 3.12 
           	-Listening on port: - 8000		
 What is the command to run your app?: -  streamlit run app.py --server.address=0.0.0.0 --server.port=8000 

- Updated the compose.yaml to hold the proper settings to connect to a local containerized Neo4j Database and Ollama server


- Ran and tested the application using a local , 
	docker containerized Neo4j container and a Ollama LLM model container , both running concurrently.
--------------------------------------------------------------------------------------------------------------------















----------------------------------------------------------------------------------------
# docker-genai-sample

A simple GenAI app for [Docker's Docs](https://docs.docker.com/) based on the [GenAI Stack](https://github.com/docker/genai-stack) PDF Reader application.
