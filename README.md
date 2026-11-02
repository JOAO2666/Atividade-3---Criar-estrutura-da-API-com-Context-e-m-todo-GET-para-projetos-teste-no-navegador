# Atividade 3 - Criar Estrutura da API com Context e Método GET para Projetos (SENAI)

Esta atividade consiste no desenvolvimento e estruturação de uma Web API utilizando **.NET 6.0**, **Entity Framework Core** e **SQL Server**, implementando a camada de acesso a dados (DbContext e Repositório) e o endpoint `GET` para listagem de projetos.

---

## 📁 Estrutura do Projeto

```plaintext
├── cria-db.sql                          # Script de criação do banco e dados iniciais
├── Exo.WebApi/
│   ├── Contexts/
│   │   └── ExoContext.cs                # Classe de contexto do Entity Framework Core
│   ├── Controllers/
│   │   └── ProjetosController.cs        # Controller da API com endpoint GET
│   ├── Models/
│   │   └── Projeto.cs                   # Model da entidade Projeto
│   ├── Repositories/
│   │   └── ProjetoRepository.cs         # Repositório de manipulação de dados de Projetos
│   ├── appsettings.json                 # Configurações da aplicação
│   ├── Exo.WebApi.csproj               # Arquivo de projeto e dependências .NET 6
│   └── Program.cs                       # Configuração de injeção de dependência e inicialização
└── README.md
```

---

## 🛠️ Tecnologias Utilizadas

- **C# / .NET 6.0**
- **ASP.NET Core Web API**
- **Entity Framework Core 6.0 (SQL Server)**
- **SQL Server / SSMS**

---

## 🗄️ 1. Configuração do Banco de Dados

1. Abra o **SQL Server Management Studio (SSMS)**.
2. Abra o arquivo [`cria-db.sql`](cria-db.sql).
3. Execute o script (`F5` ou botão **Executar**) para criar o banco de dados `ExoApi` e alimentar a tabela `Projetos`.

---

## 🚀 2. Executando a API

1. Pelo terminal, acesse a pasta `Exo.WebApi`:
   ```bash
   cd Exo.WebApi
   ```
2. Restaure as dependências e compile o projeto:
   ```bash
   dotnet restore
   dotnet build
   ```
3. Inicie o servidor:
   ```bash
   dotnet run
   ```

---

## 🌐 3. Teste no Navegador

Com a API rodando, acesse a URL gerada com o sufixo `/api/projetos`:

- `https://localhost:7154/api/projetos`
- ou `http://localhost:5038/api/projetos`

### Retorno Esperado (JSON):

```json
[
  {
    "id": 1,
    "nomeDoProjeto": "Projeto A - Obras BR",
    "area": "Construção Civil",
    "status": true
  },
  {
    "id": 2,
    "nomeDoProjeto": "Projeto B - SENAI Fest",
    "area": "Eventos",
    "status": false
  },
  {
    "id": 3,
    "nomeDoProjeto": "Projeto C - Hackathon Fest",
    "area": "Eventos",
    "status": true
  }
]
```
