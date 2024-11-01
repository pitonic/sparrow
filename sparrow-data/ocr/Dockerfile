FROM python:3.8-slim

COPY ./requirements.txt requirements.txt

RUN apt update && \
    apt install --no-install-recommends -y gcc && \
    pip install --upgrade pip && \
    pip install --no-cache-dir -r requirements.txt && \
    rm -rf /var/lib/apt/lists/*

CMD ["bash", "-c", "sleep infinity"]
#CMD ["bash", "-c", "streamlit run tracker.py"]
