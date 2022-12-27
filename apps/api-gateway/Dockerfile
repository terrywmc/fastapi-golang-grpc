FROM python:3.8-slim

# Keeps Python from generating .pyc files in the container
ENV PYTHONDONTWRITEBYTECODE=1

# Turns off buffering for easier container logging
ENV PYTHONUNBUFFERED=1

EXPOSE 8000

WORKDIR /app

COPY ./Pipfile ./Pipfile.lock /app/

RUN python -m pip install --upgrade pip
RUN pip install pipenv && pipenv install --dev --system --deploy

COPY . /app

CMD ["uvicorn", "main:app", "--proxy-headers", "--host", "0.0.0.0"]