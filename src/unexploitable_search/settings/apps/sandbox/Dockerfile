FROM python:3.10-bullseye

# Install build dependencies
RUN apt-get update && \
    apt-get install -y --no-install-recommends \
        build-essential \
        python3-dev && \
    pip install --no-cache-dir --upgrade pip && \
    pip install --no-cache-dir smolagents && \
    apt-get clean && \
    rm -rf /var/lib/apt/lists/*

# Set working directory
WORKDIR /app

# Run with limited privileges
USER nobody

# Default command
CMD ["python", "-c", "print('Container ready')"]