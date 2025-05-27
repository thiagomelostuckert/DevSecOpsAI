# DevSecOpsAI
Experimentos com inteligência artificial para melhorar o ciclo de desenvolvimento seguro. 

Sistema vulnerável: https://github.com/juice-shop/juice-shop 
Rodando o sistema vulnerável via docker: 
docker pull bkimminich/juice-shop
Run: docker run --rm -p 127.0.0.1:3000:3000 bkimminich/juice-shop
Browse: http://localhost:3000/#/ 

DAST: 
OWASP ZAP: https://www.zaproxy.org/
Rodando o  via docker: 
docker pull ghcr.io/zaproxy/zaproxy:stable
docker pull zaproxy/zap-stable

docker run --network="host" -v $(pwd):/zap/wrk/:rw -t zaproxy/zap-stable bash -c "cp /zap/wrk/zap.yaml /tmp/zap.yaml && zap.sh -cmd -addonupdate; zap.sh -cmd -autorun /tmp/zap.yaml"
