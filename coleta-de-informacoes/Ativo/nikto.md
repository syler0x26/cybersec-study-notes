# Nikto

## O que é
Scanner de vulnerabilidades web que busca falhas mais comuns, fortemente ligadas a más práticas de configuração no momento da criação do site/servidor. Faz uma análise de vulnerabilidades conhecidas.

## Por que é ativo
Envia requisições diretamente ao servidor do alvo para testar cada vulnerabilidade, fica registrado em log e pode ser detectado por firewalls/WAFs.

## Como usar
```nikto -h https://example.com```

`-h` → define o host (alvo) a ser escaneado
