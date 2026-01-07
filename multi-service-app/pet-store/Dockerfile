FROM python:alpine3.17

WORKDIR /app

COPY pet-store/app/requirements.txt .

RUN pip install --no-cache-dir -r requirements.txt

COPY pet-store/app/pet_InventoryREST.py .

ENV FLASK_APP=pet_InventoryREST.py
ENV FLASK_RUN_PORT=8000

EXPOSE 8000
CMD ["flask", "run", "--host=0.0.0.0"]