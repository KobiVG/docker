# Gebruik een officiële Python 3.9+ image als basis
FROM python:3.9-slim

# Stel de werkdirectory in de container in
WORKDIR /app

# Kopieer requirements.txt naar de werkdirectory
COPY requirements.txt .

# Installeer de Python packages die in requirements.txt staan
RUN pip install --no-cache-dir -r requirements.txt

# Kopieer de applicatiecode naar de werkdirectory
COPY app.py .

# Stel de environment variable FLASK_APP in op app.py
ENV FLASK_APP=app.py

# Stel de poort in waarop Flask zal draaien
EXPOSE 5000

# Start de Flask applicatie
CMD ["flask", "run", "-h 0.0.0.0", "-p 5000"]
