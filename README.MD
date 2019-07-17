# Github Proxy

*Docker and Docker-Compose are required*

1. Clone the app

2. Prepare token sring in view of 'token:x-oauth-basic'

3. Encode token string in base64:
```
echo -n 'token:x-oauth-basic' | base64
```

4. Get the result and put to docker-compose.yml file in 
```
    environment:
     - TOKEN=base64encodedtoken
```

5. Run app
```
sudo docker-compose up -d
```

6. Clone the private repo
```
git clone http://localhost/some/private/repo/on/github/
```
