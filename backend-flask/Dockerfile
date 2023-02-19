FROM python:3.10-slim-buster
#inside container
WORKDIR /backend-flask
#outside to inside contain
COPY requirements.txt requirements.txt

#inside container
RUN pip3 install -r requirements.txt
#copy everything from within current directory
COPY . .

ENV FLASK_ENV=development

EXPOSE ${PORT}
# command to execute when launched
CMD [ "python3", "-m" , "flask", "run", "--host=0.0.0.0", "--port=4567"]