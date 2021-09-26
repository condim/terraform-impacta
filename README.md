# terraform-impacta

#### Por alguma falha do docker, foi necessario alterar dw -p 80:8000 para --network=host, alterando no security group a porta com forwarding de 80 para 8000 e validando com http://ip_aws:8000

Obs.: analisando o problema, a causa é que o docker quando instalada, não criou a network bridge, somente a null e a host. Preferi por isso usar --network=host ao invés de debugar o porque da instalação do docker não criar a network bridge.
