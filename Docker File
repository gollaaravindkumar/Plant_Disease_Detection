FROM python:3.7
COPY . /app
WORKDIR /app
RUN pip install -r requirements.txt
# Set a default value for PORT if not provided during the build
ARG PORT=5000
ENV PORT=${PORT}
EXPOSE ${PORT}
CMD gunicorn --workers=4 --bind 0.0.0.0:${PORT} app:app