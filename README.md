# DevSecOpsAI
Experimentos com inteligência artificial para melhorar o ciclo de desenvolvimento seguro. 

 
## Clona no projeto
git clone git@github.com:juice-shop/juice-shop.git

## Compila e executa a imagem: 
cd juice-shop 
docker build -t meu-juice-shop .
docker run -d -p 3000:3000 --name meu-juice-shop-container meu-juice-shop

## URL 
http://localhost:3000/#/ 

DAST: 
OWASP ZAP: https://www.zaproxy.org/
Rodando o  via docker: 
docker pull ghcr.io/zaproxy/zaproxy:stable
docker pull zaproxy/zap-stable

docker run --network="host" -v $(pwd):/zap/wrk/:rw -t zaproxy/zap-stable bash -c "cp /zap/wrk/zap.yaml /tmp/zap.yaml && zap.sh -cmd -addonupdate; zap.sh -cmd -autorun /tmp/zap.yaml"
