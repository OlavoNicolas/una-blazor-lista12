# una-blazor-lista12
Olavo nicolas Queiroz de Paiva - Una Contagem - Ciêcias da computação
## Descrição do Projeto

O EcoStatus é uma aplicação desenvolvida em Blazor que simula ações sustentáveis realizadas pelo usuário, como reciclagem de plástico, descarte de eletrônicos e plantio de árvores.

A interface permite que o usuário interaja por meio de botões que incrementam essas ações, enquanto um sistema de pontuação acompanha o progresso total. Esse progresso é representado visualmente por uma barra, que evolui conforme as ações são realizadas.

Ao atingir um determinado valor de progresso, o sistema exibe uma mensagem de conquista, reforçando a ideia de engajamento e conscientização ambiental.

O principal objetivo do projeto é demonstrar conceitos de interatividade em aplicações web com Blazor, além de aplicar princípios de usabilidade, como feedback imediato e visibilidade do estado do sistema.

## Heurísticas de Nielsen Aplicadas

### 1. Visibilidade do Status do Sistema

O sistema mantém o usuário informado sobre o que está acontecendo:

* A barra de progresso é atualizada em tempo real
* Os valores de cada ação (plástico, eletrônico, árvores) são exibidos dinamicamente

Isso permite que o usuário compreenda imediatamente o impacto de suas ações.

---

### 2. Feedback Imediato do Usuário

Cada interação gera uma resposta imediata:

* Ao clicar nos botões, os valores são incrementados instantaneamente
* A barra de progresso responde com animação
* Uma mensagem de conquista é exibida ao atingir o objetivo

Isso melhora a experiência e mantém o usuário engajado.

---

## Guia de Execução

### Pré-requisitos

* .NET SDK versão 6 ou superior

### Passos para executar

```bash
# Clonar o repositório
git clone https://github.com/OlavoNicolas/una-blazor-lista12.git

# Entrar na pasta do projeto
cd una-blazor-lista12

# Restaurar dependências
dotnet restore

# Executar o projeto
dotnet run
```

Após executar, acesse no navegador:
http://localhost:5000
ou a porta informada no terminal.

---

## Explicação Técnica

### Uso do [Parameter] para Reutilização

O atributo [Parameter] é utilizado no Blazor para permitir que componentes recebam dados de outros componentes, tornando-os reutilizáveis.

Exemplo:

```csharp
[Parameter]
public string Titulo { get; set; }

[Parameter]
public int Valor { get; set; }

[Parameter]
public EventCallback OnClick { get; set; }
```

### Funcionamento

* Permite a passagem de dados do componente pai para o filho
* Possibilita reutilizar o mesmo componente com diferentes conteúdos
* Facilita a manutenção e organização do código

### Exemplo de uso

```razor
<CardEco Titulo="Plástico" Valor="@plastico" OnClick="IncrementarPlastico" />
```

Dessa forma, o mesmo componente pode ser utilizado diversas vezes com comportamentos diferentes.

---

## Conclusão

O projeto demonstra:

* Uso de componentes no Blazor
* Interatividade com o usuário
* Aplicação de princípios de usabilidade
* Estrutura voltada à reutilização de código

---
