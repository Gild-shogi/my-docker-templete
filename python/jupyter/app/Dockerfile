FROM python:3.11-slim

ENV PYTHONBUFFERED=1

WORKDIR /app

# python & gcc settings
RUN apt update && apt install -y \
    tzdata \
    curl \
    gcc \
    && ln -sf /usr/share/zoneinfo/Asia/Tokyo /etc/localtime \
    && apt-get clean \
    && rm -rf /var/lib/apt/lists/*

# install python packages
COPY requirements.txt /app
COPY pyproject.toml /app
RUN pip install --upgrade pip \
    && pip install --upgrade setuptools \
    && pip install -r requirements.txt

CMD ["jupyter", "lab", "--port", "8000", "--allow-root", "--ip=0.0.0.0", "--LabApp.token=''"]
