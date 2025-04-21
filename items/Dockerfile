FROM alpine:latest
RUN apk add --no-cache python3 py3-pip
WORKDIR /app
ADD requirements.pip requirements.pip
RUN python3 -m venv /app/venv
RUN source /app/venv/bin/activate && pip install -r requirements.pip
ENV PATH="/app/venv/bin:$PATH"

ADD src src

EXPOSE 5000

CMD ["python3", "src/run.py"]