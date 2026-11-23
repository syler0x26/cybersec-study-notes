# Sublist3r (Subdomínios)

## O que é
Ferramenta para enumeração de subdomínios, encontra subdomínios que o Dirb/Dirbuster não pega, já que estes buscam pastas/arquivos dentro de um domínio, enquanto o Sublist3r busca domínios inteiros associados (ex: `blog.site.com`, `api.site.com`).

>Não vem instalado por padrão, precisa baixar do repositório oficial:
## Instalação(A instalção que eu estou mostrando aqui foi feita diretamente no kali. para outros sistemas recomendo ver a documentação oficial)

🔗[Documentação oficial](https://github.com/aboul3la/sublist3r)

Caso não tenha o pip instalado:
```
sudo apt-get install python3-pip
```

Clone o repositório:
```
git clone https://github.com/aboul3la/Sublist3r.git
```

Entre na pasta clonada e instale as dependências:
```
cd sublist3r
sudo pip install -r requirements.txt
```
> referencia do repositorio do abou31a
## Como usar
```python3 sublist3r.py -d example.com -v -o nome-local-para-salvar.txt```
- `-d` → domínio alvo do scan
- `-v` → mostra na tela o que está sendo feito
- `-o` → define onde salvar o resultado
