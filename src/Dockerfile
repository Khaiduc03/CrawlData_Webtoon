FROM python:3.8 AS BUILD_IMAGE

WORKDIR /app

COPY requirements.txt requirements.txt
RUN pip install -r requirements.txt

COPY . .

COPY --from=BUILD_IMAGE /app/image ../image

CMD ["python", "webtoon_downloader.py"]
