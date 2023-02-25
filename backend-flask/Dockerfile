FROM python:3.10-slim-buster

#inside container
#make a new folder inside conatiner
WORKDIR /backend-flask


#outside the conatiner-->inside container 
#this contains the libs we wnat to run the app 
COPY requirements.txt requirements.txt

#inside the container 
#install the python images used for the app
RUN pip3 install -r requirements.txt

#outside the container --> inside the conatiner
#. means everything in the current directory 
#first period  /backend-flask represents(outside container)
#second perios /backend-flask represenst (inside the container)

COPY . .

#set EnVARS
#inside the constainer  and will remain setwhen the conatiner is running

ENV FLASK_ENV=development

EXPOSE ${PORT}

#python3 -m flask run --host=0.0.0.0 --port=4567
CMD [ "python3", "-m" , "flask", "run", "--host=0.0.0.0", "--port=4567"]