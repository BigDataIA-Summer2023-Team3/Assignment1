FROM python:3.9.13
# Pull the base docker image of python with tag 3.10.6-slim

RUN pip install --upgrade pip
# Upgrade pip package 

WORKDIR /app
# Change the working dir inside the container - cd /app

COPY intro.py requirements.txt ./
copy pages ./pages
# Copy all files from local streamlit directory to /app directory

RUN pip install -r requirements.txt
# Install the dependency

### Container Env same as local at this point
EXPOSE 8090

CMD ["streamlit", "run", "intro.py", "--server.port", "8090"]
