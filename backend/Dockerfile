FROM python:3.11.2-slim

# RUN apk update && apk add postgresql-dev gcc python3-dev musl-dev
ENV PYTHONUNBUFFERED=1

COPY . /app/
WORKDIR /app

# os-level installs
RUN apt-get update && \
    apt-get install -y \
    build-essential \
    python3-dev \
    python3-setuptools \
    libpq-dev \ 
    gcc \
    make

# venv & installs
# RUN python3 -m venv /opt/venv && \
#     /opt/venv/bin/python -m pip install pip --upgrade && \
#     /opt/venv/bin/python -m pip install -r /app/requirements.txt

# purge unused
RUN apt-get remove -y --purge make gcc build-essential \
    && apt-get autoremove -y \
    && rm -rf /var/lib/apt/lists/*

RUN pip3 install --upgrade pip
RUN pip3 install --no-cache-dir -r ./requirements.txt

EXPOSE 8080

ENTRYPOINT ["python"]
CMD ["app.py"]