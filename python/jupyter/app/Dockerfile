FROM python:3.13-slim

ENV PYTHONBUFFERED=1

WORKDIR /app

# Install uv
RUN pip install uv

# Copy dependency files
COPY pyproject.toml /app/

# Install dependencies
RUN uv sync

# Copy the rest of the application
COPY . /app/

CMD ["jupyter", "lab", "--port", "8000", "--allow-root", "--ip=0.0.0.0", "--LabApp.token=''"]

EXPOSE 8000
