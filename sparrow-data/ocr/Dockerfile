FROM python:3.7-slim

COPY ./sparrow-data/ocr/requirements.txt requirements.txt

# Install system dependencies
RUN apt-get update && apt-get install -y \
    libjpeg-dev \
    libpng-dev \
    libopenjp2-7 \
    libtiff5 \
    zlib1g-dev \
    libfreetype6-dev \
    liblcms2-dev \
    libwebp-dev \
    tk-dev \
    libharfbuzz-dev \
    ffmpeg \
    libavcodec-dev \
    libavformat-dev \
    libswscale-dev \
    libsm6 \
    libxext6 \
    libxrender-dev \
    pip install --upgrade pip && \
    pip install --no-cache-dir -r requirements.txt && \
    && rm -rf /var/lib/apt/lists/*

CMD ["bash", "-c", "sleep infinity"]
#CMD ["bash", "-c", "streamlit run tracker.py"]
