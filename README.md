🧠 Alert Router

O Alert Router é uma aplicação desenvolvida em Python com suporte a Docker, projetada para integrar e automatizar o gerenciamento de alertas do Prometheus e do Alertmanager.

🐍 Python 3

🐳 Docker / Docker Compose

📊 Prometheus

🚨 Alertmanager

📦 PostgreSQL (caso usado no ambiente de monitoramento)

🧩 Estrutura do Projeto
.
├── alert-router.py          # Lógica principal do roteamento de alertas
├── Dockerfile               # Definição da imagem da aplicação
├── docker-compose.yml       # Orquestração dos containers (app, Prometheus, Alertmanager)
├── prometheus/              # Configurações do Prometheus
│   ├── prometheus.yml
│   └── rules/
├── alertmanager/            # Configurações do Alertmanager
│   └── alertmanager.yml
├── requirements.txt         # Dependências Python
├── test-payload.json        # Payload de teste de alerta
├── result.json              # Resultado de execução ou logs gerados
└── __pycache__/             # Cache Python

🚀 Como Executar o Projeto
1️⃣ Clonar o repositório
git clone https://github.com/vitorbretz/alert-router.git
cd alert-router

2️⃣ Subir o ambiente com Docker Compose
docker compose up --build


Isso irá:

Criar os containers do Prometheus, Alertmanager e alert-router.

Configurar automaticamente as conexões e endpoints.

3️⃣ Testar o roteamento de alertas

Você pode simular o envio de um alerta executando:

python alert-router.py --test test-payload.json

📈 Monitoramento

Após a inicialização:

Prometheus: http://localhost:9090

Alertmanager: http://localhost:9093

Aplicação (Alert Router): http://localhost:8000
 (se configurada para servir via API)


💡 Aprendizados

Durante o desenvolvimento deste projeto, foram explorados conceitos essenciais como:

Configuração de ambientes de observabilidade com Prometheus e Alertmanager

Integração entre containers interdependentes via Docker Compose

Automação do gerenciamento de alertas e métricas

Boas práticas de estruturação de aplicações Python containerizadas
