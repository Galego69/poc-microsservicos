# Estrutura inicial da PoC

- `services/gateway/`: base isolada do futuro API Gateway.
- `services/usuarios/`: base isolada do futuro serviço de usuários.
- `services/pedidos/`: base isolada do futuro serviço de pedidos.
- `docker-compose.yml`: define a construção e a execução local dos três contêineres.
- `Dockerfile` em cada serviço: empacota o processo Python mínimo em uma imagem independente.
- `.gitignore`: evita registrar arquivos temporários e configurações locais.

## Critério de conclusão da Fase 1

A estrutura de pastas e os arquivos Docker estão definidos; o repositório Git local está inicializado com commit inicial; cada contêiner possui uma rota `/health` para verificação básica. O funcionamento dos contêineres precisa ser confirmado em uma máquina com Docker instalado e iniciado.
