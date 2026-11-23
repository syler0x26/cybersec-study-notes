## Dirb e Dirbuster (Brute Force URLs)
O que é

Ataque de força bruta em URLs,  a ferramenta pega vários parâmetros de uma wordlist e vai testando um por um no site alvo, tentando descobrir páginas, pastas ou arquivos que não estão visíveis publicamente.

Por que é ativo

Cada tentativa da wordlist gera uma requisição HTTP direta ao servidor do alvo, são centenas ou milhares de requisições, o que é facilmente detectável em logs de servidor e por firewalls/WAFs.

Exemplo dos parametros
```
site.com/admin 
site.com/index.php
site.com/backup
```
## Como usar o dirb
1. Baixar ou criar uma wordlist
 [Download da wordlist](coleta-de-informacoes/Ativo/Wordlist.txt)

Wordlists populares:

SecLists (GitHub), coleção enorme de wordlists prontas
/usr/share/wordlists/dirb/ , já vem com algumas listas padrão em sistemas tipo Kali Linux

2. Rodar o Dirb no terminal
   
```dirb https://example.com wordlist.txt```

## Como usar o Dirbuster

É a mesma lógica do Dirb, só que com painel gráfico, mais visual, permite configurar threads, extensões de arquivo a testar (.php, .html, .txt) e ver o progresso em tempo real.

Observação
> Teste apenas em ambientes autorizados. Sites como testphp.vulnweb.com (Acunetix) e o DVWA (Damn Vulnerable Web Application) são feitos de propósito pra esse tipo de prática.
