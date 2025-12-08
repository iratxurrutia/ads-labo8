#imagen base
FROM python:alpine

#directorio de trabajo
WORKDIR /code

#variables de entorno
ENV FLASK_APP=app.py
ENV FLASK_RUN_HOST=0.0.0.0

#instalar dependencias
RUN apk add --no-cache gcc musl-dev linux-headers

#copiar requirements.txt en /code
COPY requirements.txt .

#instalar dependencias de python
RUN pip install -r requirements.txt

#copiar app.py en /code
COPY app.py .

CMD ["flask", "run"]
