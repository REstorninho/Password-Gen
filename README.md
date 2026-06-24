# Gerador de Passwords Seguras 🔐

Aplicação web simples, totalmente client-side, para gerar passwords seguras e calcular os respetivos hashes.

## Funcionalidades

- Geração de passwords com comprimento configurável (8 a 64 carateres)
- Seleção de tipos de carateres:
  - Letras maiúsculas (A-Z)
  - Letras minúsculas (a-z)
  - Números (0-9)
  - Símbolos (`!@#$%^&*()_+-=[]{}|;:,.<>?`)
- Opção para excluir carateres ambíguos (`l`, `1`, `I`, `O`, `0`)
- Indicador visual da força da password
- Cálculo automático de hashes da password gerada: MD5, SHA-1, SHA-256, SHA-384 e SHA-512
- Botões de cópia rápida para a password e para cada hash

## Como usar

Basta abrir o ficheiro [`index.html`](./index.html) num browser — não há dependências nem necessidade de build ou servidor.

```bash
# Exemplo: abrir diretamente no browser
xdg-open index.html   # Linux
open index.html       # macOS
start index.html      # Windows
```

## Segurança

- A geração de carateres usa `crypto.getRandomValues`, a API criptográfica segura do browser, em vez de `Math.random()`.
- Toda a lógica corre localmente no browser — nenhuma password é enviada para qualquer servidor.
- O MD5 é incluído apenas por compatibilidade/referência; **não** deve ser usado para fins de segurança, dado estar criptograficamente quebrado.

## Tecnologias

- HTML, CSS e JavaScript puro (vanilla), sem frameworks ou dependências externas.
