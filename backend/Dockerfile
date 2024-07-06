FROM python:3.11-alpine

RUN curl -sSL https://install.python-poetry.org | python3 -

WORKDIR /app

COPY pyproject.toml poetry.lock ./

RUN poetry install

COPY . .

RUN poetry run bash ./prestart.sh


CMD ["poetry", "run", "app.main:app", "--reload"]
