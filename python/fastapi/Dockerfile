FROM python:3.13-slim

ENV PYTHONBUFFERED=1

WORKDIR /app

# Install uv
RUN pip install uv

# Copy dependency files
COPY pyproject.toml /app/
COPY uv.lock /app/

# Install dependencies
RUN uv sync --frozen --no-dev

# Copy the rest of the application
COPY ./app /app/app

CMD ["uv", "run", "uvicorn", "app.main:app", "--host", "0.0.0.0", "--port", "8000"]

EXPOSE 8000
