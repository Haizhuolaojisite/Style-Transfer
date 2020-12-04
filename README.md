# Style-Transfer

Serving a Machine Learning Model with FastAPI and Streamlit

## Download Models

Use the package manager [pip](https://pip.pypa.io/en/stable/) to install fast-style transfer models.

```bash
sh download_models.sh
```

## Usage

### From the "backend" folder in terminal, build the image
```python
docker build -t backend .
```

### Run the container:
```python
$ docker run -p 8080:8080 backend

INFO:     Started server process [1]
INFO:     Waiting for application startup.
INFO:     Application startup complete.
INFO:     Uvicorn running on http://0.0.0.0:8080 (Press CTRL+C to quit)
```

### In the browser, navigate to http://localhost:8080/. You should see:
```
{
  "message": "Welcome from the API"
}
```
kill the container once done

### To test, from the project root, build the images and spin up both containers, then navigate to http://localhost:8501
```
$ docker-compose up -d --build
```

![Image of styletransfer](https://j.gifs.com/ROAxyE.gif)


## Reference
https://testdriven.io/blog/fastapi-streamlit/