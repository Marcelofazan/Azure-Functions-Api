## ⚙️ Azure-Functions-Api
Exemplo de criar  HTTP Trigger Azure Functions com funções REST em C# .NET Core 10 EF com banco de dados SQL-Server.

#### 🎨 Aqui está uma demonstração do projeto
<img width="600" height="350" alt="Azure_Functions" src="https://github.com/user-attachments/assets/b385b370-e67a-407c-9aca-08adb29f961a" />

#### 📋 O que você vai encontrar neste projeto

| Tecnologia| Descrição |
|-----------|-----------|
| Azure Functions | Arquitetura serverless, com uso de gatilhos de API (HTTP Triggers) |
| Computação em Nuvem | Infraestrutura global de data centers para hospedar, gerenciar e escalar aplicativos e dados pela internet |

#### 💬 Requisitos do Projeto
- Necessário Emulador Azurite instalado
- Realizar Migrations EntityFramework .NET
  
#### ⚠️ String de conexão do banco
Modifique a string de conexão no arquivo local.settings.json se caso necessário, no trecho indicado:
```bash 
"Server=localhost\\SQLEXPRESS;Database=Shop;Trusted_Connection=True;TrustServerCertificate=True;"
```

#### 🔄 Executar a aplicação

- Criar Migrations EntityFramework no Visual Studio e Update da database SQLServer .

```bash 
Install-Package Microsoft.EntityFrameworkCore.Tools
Add-Migration InitialCreate -StartupProject "ApiFunctionsAzure"
Update-Database -StartupProject "ApiFunctionsAzure"
```

#### 🧪 Executar Functions
Importar Coleção de testes que contém no diretório Postman **APIFunctionsAzure.postman_collection**

| Metodo | Descrição |
|-----------|-----------|
| RegistrarProduto: [POST] | http://localhost:7006/api/RegistrarProduto|
| BuscarProdutos: [GET] | http://localhost:7006/api/BuscarProdutos |
| BuscarProduto: [GET] |  http://localhost:7006/api/BuscarProduto/{id} |
| AtualizarProduto: [PUT] | http://localhost:7006/api/AtualizarProduto |
| ApagarProduto: [DELETE] | http://localhost:7006/api/ApagarProduto/{id} |

