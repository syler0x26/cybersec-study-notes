# Dig

## O que é
Ferramenta de consulta DNS, similar ao nslookup, mas com saída mais detalhada. Permite buscar diferentes tipos de registro e testar configurações de segurança do DNS, como transferência de zona.

## Como usar

### Buscar e-mails (registro MX)
```dig globo.com -t mx```

### Buscar servidores DNS (registro NS)
```dig globo.com -t ns```

### Testar transferência de zona (AXFR)
Transferência de zona é quando um servidor DNS mal configurado permite que qualquer um baixe o mapa completo de subdomínios do domínio,  uma falha grave de configuração.

```dig axfr zonetransfer.me @nameserver-do-dns```

## Por que é (majoritariamente) passivo
Consultas de registro (MX, NS) não tocam diretamente na infraestrutura do alvo, só nos servidores DNS públicos. Já o teste de transferência de zona interage diretamente com o servidor DNS do próprio alvo — por isso alguns consideram essa parte específica como uma técnica de fronteira entre passivo e ativo.

## Site de apoio
> esse site permite fazer essas varreduras, porem é mai interessante fazer pelo terminal do kali pela sua vasta flexibilidade

🔗[Site de apoio](https://mxtoolbox.com)
