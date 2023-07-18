FROM python:3.11

ENV PYTHONUNBUFFERED=1

WORKDIR /app

RUN pip install --upgrade pip "poetry==1.4.2"
RUN poetry config virtualenvs.create False --local
COPY pyproject.toml poetry.lock ./
RUN poetry install

COPY mysite .

CMD ["python", "manage.py", "runserver"]