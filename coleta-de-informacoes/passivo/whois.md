# Whois

## O que é
Consulta a bancos de dados públicos de registro de domínios, que trazem informações sobre o proprietário, data de registro/expiração, servidores DNS associados e, às vezes, dados de contato.

## Por que é passivo
Você consulta um banco de dados de terceiros (os registradores de domínio) - não há nenhuma interação direta com o servidor ou sistema do alvo. Por isso, essa técnica não é detectável pelo alvo.

## Informações que pode revelar
- Nome do registrante (quando não há privacidade ativada)
- Data de criação e expiração do domínio
- Servidores de nomes (name servers) usados
- Registrador (empresa onde o domínio foi registrado)
- Às vezes, e-mail e telefone de contato

## Como usar

### Via terminal (Linux)
\`\`\`bash
whois exemplo.com
\`\`\`

### Via sites
- https://whois.domaintools.com/
- https://who.is/

## Observação
Muitos domínios hoje usam "privacidade WHOIS" (WHOIS privacy/proxy), que esconde os dados reais do proprietário atrás de um serviço de proteção - nesses casos, o retorno vem com dados genéricos da empresa de proteção, não do dono real.
