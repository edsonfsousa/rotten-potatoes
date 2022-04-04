FROM python:3.8--slim-burster
WORKDIR /app
COPY requirements ./
RUN python -m pip install -r requirements.txt7
COPY . /app
EXPOSE 50000
CMD [ "gunicorn", "--workers=3", "--bind", "0.0.0.0:50000", "-c", "config.py", "app:app" ]