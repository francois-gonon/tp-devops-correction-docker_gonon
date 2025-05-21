# TP DevOps Correction Docker
This project is now mine 

2-1 What are testcontainers?
test containers are java libs that start docker images to test code in the actual environment it is destined to be ran in 

2-2 For what purpose do we need to use secured variables ?
We must not put token and logins etc. in clear, hard coded in codebase to 1 : not leak the token 2 : potentially use a different token / environment layout for testing

2-3 Why did we put needs: build-and-test-backend on this job? Maybe try without this and you will see!
It ensures images are only pushed if test are successful and test are stopping when tehy encounter an error

2-4 For what purpose do we need to push docker images?
We push doker images with commands in main.yml so that the newest version of images is pushed to dockerhub when we pushed on github,rendering the images immediately available 

Questions for TP3 : 

Is it really safe to deploy automatically every new image on the hub ? explain. What can I do to make it more secure?

pushing every image can be dangerous because there are no verification step and any merge/accidental edits to tamper with the codebase
