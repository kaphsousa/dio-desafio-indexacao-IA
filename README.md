# Desafio: Conhecimento com Azure AI Search

## 🧩 Resumo do Desafio

Neste projeto, fomos desafiados a criar uma solução de mineração de conhecimento utilizando o **Azure AI Search**. O objetivo era organizar e explorar automaticamente um conjunto de avaliações de clientes de uma cafeteria fictícia, extraindo informações relevantes a partir de documentos armazenados. Aplicamos técnicas de **ingestão, enriquecimento com IA** e **indexação de dados** para facilitar buscas inteligentes e obter insights sobre a experiência do cliente.

## 🛠️ Tecnologias/Ferramentas Utilizadas

- **Azure AI Search**: Para indexação e buscas semânticas
- **Azure AI Services (Cognitive Services)**: Para enriquecimento com IA (extração de sentimentos, frases-chave, OCR, etc.)
- **Azure Blob Storage**: Para armazenar os documentos originais e enriquecidos
- **Azure Portal**: Interface gráfica para configurar todos os serviços
- **Search Explorer**: Para testar e validar buscas na base indexada

## 📥 Passo a Passo da Ingestão e Indexação

1. **Criar os recursos no Azure**:
   - Azure AI Search
   - Azure AI Services (na mesma região)
   - Storage Account com contêiner de blobs

2. **Upload dos documentos**:
   - Enviar os arquivos de avaliações para o container `coffee-reviews`

3. **Indexação automatizada com enriquecimento**:
   - Usar o assistente “Importar dados” no AI Search
   - Conectar ao blob storage
   - Anexar habilidades cognitivas (OCR, sentimento, entidades)
   - Salvar enriquecimentos no “Knowledge Store”
   - Definir o índice e o indexador (`coffee-index`, `coffee-indexer`)

4. **Consulta aos dados indexados**:
   - Utilizar o Search Explorer com consultas JSON
   - Buscar por localização, sentimento, palavras-chave, etc.

## 💡 Insights Obtidos

- Identificamos sentimentos negativos em apenas 1 das avaliações.
- Analisando as **frases-chave** dessa avaliação negativa, foi possível detectar possíveis causas de insatisfação.
- As **localizações mais mencionadas** pelos clientes também foram mapeadas, revelando padrões geográficos de atendimento.
- **Tags e legendas geradas por imagem** também ajudaram na análise dos dados visuais dos documentos.

## 🚀 Como Executar o Projeto

Este projeto é baseado em recursos no Azure, portanto é necessário:

1. Ter uma conta ativa no [Microsoft Azure](https://portal.azure.com/)
2. Seguir o guia interativo do laboratório em: [Lab no GitHub](https://microsoftlearning.github.io/mslearn-ai-fundamentals/Instructions/Labs/11-ai-search.html)
3. Recomenda-se iniciar pelo Azure Portal e seguir o fluxo visual do assistente de importação de dados.
