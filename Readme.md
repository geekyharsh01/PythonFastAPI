---------------------------------------**--Steps to Run the API--**---------------------------------------------------------

1)Open terminal in this directory and then install all the requirements on your pc using command - pip install -r requirements.txt 

2)Then move to directory api and then run the api using command -  uvicorn main:app --reload

3)Then it will host the api on the free port on your pc, either do control+click on the link in the terminal or you can copy paste that link in browser.

4) Go to http://127.0.0.1:8000/docs, here link before docs is the link given in your terminal just add /docs ahead of it and you will be directed to FastAPI- Swagger UI
there you can use all the functionalities implemented.

----------------------------------------------------------------------------------------------------------------------------
In the .\api\main.py containes the api endpoints : 
1) POST / detect_cellphone - This end point takes image as input and returns cellular telephone if it contains the cellphone.

2) GET / detected_cellphone - All the predictions that are done by the detect_cellphone endpoints are stored in the list which can be retrieved using this endpoint by inputting the index , if index out of range it will show.

Created a ApiCheck.html, if API server is on then requests can be send throught this webpage and the results can be retrieved from the api.

In the .\api\models.py contains the resnet-50 model which is used to predict the cellphone for the input image.
------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

**Steps to RUN Docker and build docker image and make and run a container**
This repository Contains the dockerfile which includes the code to build a docker image that can be used to open the python fastAPI app created previously. Find the link of the Python Project FastAPI - https://github.com/geekyharsh01/Python_Project How to run the dockerfile and then finally run the FastAPI app: step1- Download this repository.

Step3- If you have'nt installed Docker Desktop then install it and then run it. Step4- open terminal in the directory where dockerfile is present and type the command - 
" **docker build -t yourImageName . **" Don't forget to put dot at end as it is shown in the command, after running this command , It will take some time to build the image for you.

After creating the image , you can type "docker images"  to see the your built image of this application.

Step5- Go to the Docker Desktop and in the images you can see your built image with name yourImageName , Now Run that image and in the optional settings Put 8000 or any other suitable port you like and then Run the image , It will create a container and the program inside it will start running.
Or you can use commmand line - " docker run -d -p 8000:8000 --name nameofcontainer pythonfastapi "

Step6- Access your web Appilcation by clicking on the 8000:8000 this kind of link shown in the docker Desktop at the top of the log which you see when the container is running. or you can access at localhost:yourport , yourport is the port number you gave earlier while running the image in the optional settings.



   
