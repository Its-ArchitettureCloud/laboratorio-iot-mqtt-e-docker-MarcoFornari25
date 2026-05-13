FROM python:3.11-slim
WORKDIR /app
RUN pip install paho-mqtt requests
COPY sensor.py .
COPY sensorHttp.py .
CMD ["sh", "-c", "if [ \"$PROTOCOL\" = 'http' ]; then python sensorHttp.py; else python sensor.py; fi"]
