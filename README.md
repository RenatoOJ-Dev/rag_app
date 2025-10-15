# RAG_project — Usando APIs do Google

Este é um README inicial para o projeto. Ele contém instruções básicas de instalação, configuração e execução dos exemplos presentes no repositório. Você pode editar e expandir este documento conforme o projeto evoluir.

## Visão geral

Repositório de testes e experimentos para usar APIs do Google (ex.: Google Cloud, Google APIs, Gemini/LLMs) em Python. Contém scripts de exemplo e uma pasta `data/` com arquivos de dados.

Estrutura básica:

- `dia1_teste_gemini.py` — exemplo de teste inicial (nome descritivo, ver o conteúdo do arquivo para detalhes).
- `dia2_carregar_dados.py` — script para carregar/processar dados.
- `data/` — arquivos de dados usados localmente (ex.: `dados_empresa.txt`).
- `.envexemplo` — exemplo de variáveis de ambiente (copiar para `.env`).
- `.gitignore` — regras para evitar commitar credenciais, ambientes virtuais e arquivos temporários.

## Requisitos

- Python 3.8+ recomendado
- Recomenda-se usar um ambiente virtual (venv/virtualenv/conda)
- Dependências do projeto listadas em `requirements.txt` (instalar com pip)

## Instalação rápida

1. Criar e ativar um ambiente virtual:

```powershell
python -m venv .venv
.\.venv\Scripts\Activate.ps1
```

2. Instalar dependências:

```powershell
pip install -r requirements.txt
```

3. Copiar o arquivo de exemplo de variáveis de ambiente:

```powershell
copy .envexemplo .env
```

4. Preencher `.env` com suas credenciais e chaves (veja a seção abaixo).

## Configuração de credenciais e `.env`

O repositório contém um arquivo `.envexemplo` com variáveis de exemplo. Copie para `.env` e preencha com seus valores:

- `GOOGLE_API_KEY`: chave simples de API (se aplicável)
- `GOOGLE_APPLICATION_CREDENTIALS`: caminho para o JSON da conta de serviço (opcional)
- `GOOGLE_OAUTH_CLIENT_ID` e `GOOGLE_OAUTH_CLIENT_SECRET`: se usar OAuth2

Importante: nunca commit seu `.env` real ou arquivos de credenciais (ex.: `service-account.json`). O `.gitignore` já está configurado para ignorar esses arquivos.

## Como rodar os scripts de exemplo

Abra o terminal com o ambiente virtual ativado e rode:

```powershell
python dia1_teste_gemini.py
python dia2_carregar_dados.py
```

Veja o conteúdo dos scripts para entender os parâmetros e saídas — alguns scripts podem depender das variáveis do `.env` ou de arquivos em `data/`.

## Boas práticas

- Não versionar arquivos com credenciais.
- Use `virtualenv`/`.venv` para isolar dependências.
- Documente neste README comandos e fluxos importantes enquanto o projeto evolui.

## Próximos passos sugeridos

- Adicionar exemplos específicos para autenticação com Google (OAuth2 e Service Account).
- Adicionar testes automatizados e um script de exemplo para carregar dados de `data/`.
- Incluir instruções para deployment (se necessário).

---

Se quiser, eu já posso:
- Adicionar uma seção detalhada mostrando como criar uma conta de serviço no Google Cloud e gerar o JSON de credenciais.
- Atualizar o README para permitir que `data/dados_empresa.txt` seja versionado (se quiser compartilhar esse arquivo).
# RAG_project
