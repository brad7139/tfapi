# Sentiment Analysis (Convonutional Neural Network model) using Tensorflow

## Docker Setup
0. Install [Docker](https://docs.docker.com/engine/installation/)
1. Run `git clone git@github.com:ggodreau/tfapi.git`
2. Open docker terminal and navigate to `/path/to/tf-sentiment-docker`
3. Run `docker build . -t tfapi`
4. Run `docker run -p 8080:8180 sentiment-api`
5. Run `curl -vvv 'http://localhost:8080/sentiment?senderName=greg&message=stunning%20adore%20products%20great'
6. 
```*   Trying ::1...
* TCP_NODELAY set
* Connected to localhost (::1) port 8080 (#0)
> GET /sentiment?senderName=greg&message=stunning%20adore%20youproductsgreat HTTP/1.1
> Host: localhost:8080
> User-Agent: curl/7.52.1
> Accept: */*
> 
< HTTP/1.1 200 OK
< Content-Type: application/json
< Transfer-Encoding: chunked
< Date: Fri, 05 Oct 2018 15:52:01 GMT
< Server: localhost
< 
* Curl_http_done: called premature == 0
* Connection #0 to host localhost left intact
{"Name": "greg", "Sentiment": "Positive", "Response": "Thank you for your valuable feedback! \n \nIt will help us to serve better in future.\n"}```

7. Kill your container with `docker stop $(docker ps -aq)`
