FROM python:3.10-slim-buster

WORKDIR /backend-flask

COPY requirements.txt requirements.txt
RUN pip3 install -r requirements.txt

COPY . .

# Set environment defaults
ENV FRONTEND_URL="http://frontend-react-js:3000" \
    BACKEND_URL="http://backend-flask:4567" \
    FLASK_ENV=development

EXPOSE ${PORT}
CMD [ "python3", "-m" , "flask", "run", "--host=0.0.0.0", "--port=4567"]
