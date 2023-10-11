# Language Detection using FastAPI and Scikit-Learn

This project demonstrates an example of using FastAPI and Scikit-Learn to detect the language of a given text. The project provides an API endpoint /predict that accepts a text string in the request and returns the predicted language of the text.

## Running the Project

Build docker image:
```bash
docker build -t language-detection .
```

Run docker container:
```bash
docker run -p 8000:8000 --name language-detection --rm language-detection
```

Try prediction via curl
```bash
curl -X 'POST' \
  'http://localhost:8000/predict' \
  -H 'accept: application/json' \
  -H 'Content-Type: application/json' \
  -d '{
  "text": "El oso no come pescado en octubre"
}'
```

or via swagger:

http://localhost:8000/docs