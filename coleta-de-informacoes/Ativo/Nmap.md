Nmap
O que é

Ferramenta de varredura de rede usada para descobrir hosts ativos, portas abertas, serviços rodando e, em alguns casos, até o sistema operacional do alvo.

Por que é ativo

Nmap envia pacotes diretamente para o alvo e analisa as respostas. Essa interação direta pode ser detectada por firewalls, IDS/IPS e logs do sistema.

Informações que pode revelar
Portas abertas e fechadas
Serviços rodando em cada porta (ex: HTTP, SSH, FTP)
Versão dos serviços (em alguns casos)
Sistema operacional estimado
Hosts ativos em uma rede
Como usar
Varredura salvando em um arquivo

```nmap exemplo.com -oN name_folder.txt```

Varredura detectando o sistema operacional

```sudo nmap -O exeplo.com```
Varredura básica:

```nmap exemplo.com```

Varredura com detecção de versão de serviços:

```nmap -sV exemplo.com```

Varredura de todas as portas:

```nmap -p- exemplo.com```

Varredura "silenciosa" (menos detectável):

```nmap -sS exemplo.com```

# Nmap Scripting Engine (NSE)

O Nmap tem um sistema de scripts chamado NSE (Nmap Scripting Engine), que permite automatizar tarefas além da varredura básica, como detectar vulnerabilidades conhecidas, testar força bruta de login, coletar informações extras de um serviço, entre outros.

Sintaxe básica
```sudo nmap --script <nome-do-script> <alvo>```

Onde encontrar os scripts

Todos os scripts disponíveis (mais de 600) estão documentados oficialmente no site do Nmap, com descrição de cada um, categoria e exemplos de uso:

🔗 https://nmap.org/nsedoc/

Categorias de scripts

Os scripts são organizados por categoria, e dá pra rodar uma categoria inteira de uma vez em vez de um script específico:

sudo nmap --script vuln scanme.nmap.org

Principais categorias:

auth - testes de autenticação

vuln - detecção de vulnerabilidades conhecidas

discovery - descoberta de informações adicionais do alvo

brute - ataques de força bruta

safe - scripts considerados seguros, sem risco de causar instabilidade no alvo

- Observações:
> Alguns scripts (principalmente das categorias vuln e brute) podem ser considerados intrusivos e gerar impacto real no alvo. Use apenas em ambientes autorizados.

>Varrer redes ou hosts sem autorização é crime em diversos países, incluindo o Brasil (invasão de dispositivo informático - Lei 12.737/2012). Use somente em ambientes próprios ou com autorização explícita (ex: laboratórios como TryHackMe, HackTheBox).
