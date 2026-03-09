# 🍕 Pizza Tracker

![Status do Projeto](https://img.shields.io/badge/status-em%20desenvolvimento-yellow)
![Go Version](https://img.shields.io/github/go-mod/go-version/Gomaozao/pizza-tracker)

Sistema full-stack para rastreamento de pedidos de pizza em tempo real. Permite que clientes façam pedidos e acompanhem seu status usando um ID, enquanto administradores recebem notificações instantâneas de novos pedidos via Server-Sent Events (SSE).

##  Funcionalidades

-   **Pedido de Pizza**: Interface para clientes realizarem novos pedidos.
-   **Rastreamento em Tempo Real**: Acompanhamento do status do pedido (preparando, saiu para entrega, entregue) através de um ID único.
-   **Notificações para Administradores**: Recebimento instantâneo de novos pedidos na interface administrativa, sem necessidade de recarregar a página, usando **Server-Sent Events (SSE)**.
-   **Autenticação**: Sistema de login para acesso à área administrativa (`user logged checker`).
-   **Atualizações ao Vivo**: A página do administrador é atualizada em tempo real com a chegada de novos pedidos.

##  Tecnologias Utilizadas

-   **Backend**: [Go](https://golang.org/) (Estrutura de pastas com `cmd`, `internal`, `data`)
-   **Templates HTML**: Renderização no servidor com a pasta `templates`
-   **Comunicação em Tempo Real**: Server-Sent Events (SSE) para notificações unidirecionais do servidor para o cliente.
-   **Armazenamento**: Estrutura inicial baseada em arquivos (pasta `data`), facilitando a prototipagem.

##  Como Executar o Projeto

### Pré-requisitos
-   [Go](https://golang.org/dl/) (versão compatível com o módulo, veja em `go.mod`)
-   Git

1.  **Clone o repositório:**
    ```bash
    git clone https://github.com/Gomaozao/pizza-tracker.git
    cd pizza-tracker

2. Instale as dependências:
  O Go Modules gerenciará isso automaticamente.
  ```bash

  go mod download

# Execute a aplicação:
O ponto de entrada da aplicação está na pasta cmd.
```bash

go run cmd/main.go


# Acesse no navegador:

    Página do Cliente (fazer pedido): http://localhost:8080 (ou a porta configurada)

    Área do Administrador: http://localhost:8080/admin (será necessário fazer login)
