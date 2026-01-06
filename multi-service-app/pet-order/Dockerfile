FROM python:alpine3.17

WORKDIR /app

COPY app/requirements.txt . 

RUN pip install --no-cache-dir -r requirements.txt

COPY app/pet_order.py .

ENV FLASK_APP=app/pet_order.py
ENV FLASK_RUN_PORT=8080

EXPOSE 8080
CMD ["flask", "run", "--host=0.0.0.0"]