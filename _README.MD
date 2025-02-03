<table align="center">
    <tr>
        <td align="center" width="25%">
            <img src="./MegaApiDotnetCore/_docs/assets/Imagem1.png" >
        </td>
        <td align="center" width="75%">
          
# MegaMan Bosses API
          
[![Release workflow](https://github.com/user/megaman-api/actions/workflows/release.yml/badge.svg)](https://github.com/user/megaman-api/actions/workflows/release.yml)
[![Latest release](https://img.shields.io/github/v/release/user/megaman-api)](https://github.com/user/megaman-api/releases/latest)
  <br>
[![Build Status](https://github.com/user/megaman-api/actions/workflows/build.yml/badge.svg)](https://github.com/user/megaman-api/actions/workflows/build.yml)
        </td>
    </tr>
</table>

<p align="center">
  MegaMan Bosses API é um backend desenvolvido em .NET Core 3.1 para fornecer informações sobre chefes da franquia MegaMan.
  O projeto disponibiliza dados no formato JSON e é ideal para aplicações que necessitam dessas informações.
  <br />
</p>

## Exemplo de JSON retornado
```json
{
    "Id": 1,
    "Code": "DLN/DRN-003",
    "Name": "Cutman",
    "HP": 150,
    "Picture": "https://vignette.wikia.nocookie.net/megaman/images/2/22/Cutman.png"
}
```

## Tecnologias Utilizadas
- **.NET Core 3.1**
- **Banco de Dados SQL Server**

### Dependências
| Dependência | Versão | Link |
|-------------|---------|------|
| [Microsoft.EntityFrameworkCore](https://www.nuget.org/packages/Microsoft.EntityFrameworkCore/) | 3.1.8 |
| [Microsoft.EntityFrameworkCore.Design](https://www.nuget.org/packages/Microsoft.EntityFrameworkCore.Design/) | 3.1.8 |
| [Microsoft.EntityFrameworkCore.SqlServer](https://www.nuget.org/packages/Microsoft.EntityFrameworkCore.SqlServer/) | 3.1.8 |
| [Newtonsoft.Json](https://www.nuget.org/packages/Newtonsoft.Json/) | 12.0.2 |

## Como Executar o Projeto
### 1. Clonar o repositório
```sh
git clone <URL_DO_REPOSITORIO>
cd <NOME_DO_PROJETO>
```

### 2. Restaurar dependências
```sh
dotnet restore
```

### 3. Configurar o banco de dados
Adicione a string de conexão no `appsettings.json`.
```json
"ConnectionStrings": {
    "DefaultConnection": "Server=SEU_SERVIDOR;Database=MEGA_MAN_DB;User Id=USUARIO;Password=SENHA;"
}
```

### 4. Executar as migrações do banco de dados
```sh
dotnet ef database update
```

### 5. Rodar o projeto
```sh
dotnet run
```

A API estará disponível em `http://localhost:5000` ou `https://localhost:5001`.

## Endpoints da API
### Listar todos os robôs
**GET** `/api/v1/robots`

### Buscar robô por ID
**GET** `/api/v1/robots/{id}`

### Criar um novo robô
**POST** `/api/v1/robots`

## Licença
Este projeto é licenciado sob a [MIT License](LICENSE).

## Autor
Vinicius Victorio (https://github.com/ViNiciusVicTorio1).

