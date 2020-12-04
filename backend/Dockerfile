# download using the Slim version,takes about 500Mb, which is a middle ground between alpine and the base version.
FROM python:3.8-slim

# terminal will start from this default directory
WORKDIR /app

#'ffmpeg', 'libsm6', and 'libxext6' are required for OpenCV.
RUN apt-get update
RUN apt-get install \
    'ffmpeg'\
    'libsm6'\
    'libxext6'  -y

# copy and install libraries
COPY requirements.txt .
RUN pip install -r requirements.txt

COPY . .

EXPOSE 8080

CMD ["python", "main.py"]