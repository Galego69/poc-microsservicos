# PoC de Microsserviços — Fase 1: Início

**Responsável:** Nicolas  
**Prazo previsto no cronograma:** 09/10  
**Objetivo desta fase:** preparar a estrutura inicial do projeto, criar os arquivos Docker e deixar o repositório Git inicializado.

> Esta entrega cobre somente a infraestrutura inicial. A lógica de negócio, o CRUD e a comunicação entre os microsserviços ficam para as próximas fases.

## Estrutura de pastas

```text
poc-microsservicos-fase1/
├── .gitignore
├── README.md
├── docker-compose.yml
├── docs/
│   └── estrutura.md
└── services/
    ├── gateway/
    │   ├── Dockerfile
    │   └── app.py
    ├── usuarios/
    │   ├── Dockerfile
    │   └── app.py
    └── pedidos/
        ├── Dockerfile
        └── app.py
```

## Pré-requisitos

- Git instalado;
- Docker Desktop instalado e iniciado (Windows/macOS) ou Docker Engine com Docker Compose.

## Como iniciar os contêineres

Abra um terminal nesta pasta e execute:

```bash
docker compose up --build -d
```

Confira o estado dos serviços:

```bash
docker compose ps
```

As rotas de verificação inicial são:

- Gateway: http://localhost:8000/health
- Usuários: http://localhost:8001/health
- Pedidos: http://localhost:8002/health

Cada rota deve retornar JSON indicando que o processo está ativo. Nesta fase, elas são apenas verificações de saúde: não há CRUD nem comunicação entre serviços implementados.

Para parar e remover os contêineres:

```bash
docker compose down
```

## Conferir o repositório Git

O pacote já inclui um repositório Git local com o commit inicial. Dentro desta pasta, execute:

```bash
git status
git log --oneline
```

Para publicar no GitHub, crie um repositório remoto vazio e siga as instruções da plataforma para conectar o remoto. Nenhum repositório remoto foi criado por esta entrega.
