install traefik locally with certificates

```sh
mkcert -cert-file certs/local-cert.pem \
  -key-file certs/local-key.pem \
  "app.localhost" "*.app.localhost" \
  "domain.local" "*.domain.local"

cd certs
mkcert -install

cd ..
docker compose up -d 
```
