FROM python:3.11-slim

WORKDIR /app

# Copy dependency definition and install
COPY req.txt .
RUN pip install --no-cache-dir -r req.txt

# Copy application files
COPY . .

# Expose default FastAPI/Flask/Uvicorn port
EXPOSE 5000

# Update this CMD depending on your framework (example shown for FastAPI/Uvicorn)
CMD ["uvicorn", "main:app", "--host", "0.0.0.0", "--port", "5000"]