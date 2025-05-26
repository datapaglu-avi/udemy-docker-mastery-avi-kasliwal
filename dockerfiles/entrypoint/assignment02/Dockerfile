FROM python:slim

WORKDIR /app

COPY ./requirements.txt .

RUN pip install --no-cache-dir -r requirements.txt

COPY . .

VOLUME /app/data

ENTRYPOINT [ "./docker-entrypoint.sh" ]

CMD ["uvicorn", "main:app", "--host", "0.0.0.0", "--port", "8000"]

# docker image build -t datapagluavi/fastapi:assignment_solve .
# docker container run -d -p 8000:8000 --name fastapi datapagluavi/fastapi:assignment_solve