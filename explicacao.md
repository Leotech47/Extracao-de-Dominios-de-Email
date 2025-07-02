Aqui está o código completo e funcional, conforme a descrição da tarefa:

```python
# Recebe a entrada e armazena na variável "entrada" 
entrada = input()

# Função responsável por extrair os domínios dos emails
def extrair_dominios(emails):
    # Separa os emails por ponto e vírgula
    lista_emails = emails.split(';')
    
    # Extrai a parte após o '@' de cada email
    dominios = [email.split('@')[1] for email in lista_emails if '@' in email]
    
    return dominios

# Imprime a lista de strings com os domínios
print(extrair_dominios(entrada))
```

✅ **Explicação da linha principal da lógica:**

```python
[email.split('@')[1] for email in lista_emails if '@' in email]
```

* Garante que o email tenha `@`.
* Separa o email em duas partes e retorna apenas a parte do domínio (após o `@`).

Esse código cobre os casos descritos nos exemplos e pode ser facilmente testado com entradas como:

```
ana@example.com;bob@test.com
```

Saída:

```
['example.com', 'test.com']
```
