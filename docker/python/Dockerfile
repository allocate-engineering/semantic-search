FROM jupyter/minimal-notebook
# python:3.11-slim

WORKDIR /app

# Use faster installs + cache
RUN pip install --upgrade pip
COPY docker/python/requirements.txt .
RUN pip install -r requirements.txt

COPY . .

CMD ["bash"]
