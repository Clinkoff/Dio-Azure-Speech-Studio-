# Dio-Azure-Speech-Studio-

### 1. **Análise de Sentimentos**  
   - **Funcionalidade**: Identificar emoções (positivo, negativo, neutro) em textos.  
   - **Aplicação**:  
     ```python
     # Exemplo de uso via SDK
     from azure.ai.textanalytics import TextAnalyticsClient
     client = TextAnalyticsClient(endpoint=endpoint, credential=credential)
     result = client.analyze_sentiment(["Adorei o atendimento, mas o produto chegou atrasado."])
     print(result.confidence_scores)  # Saída: Positivo (75%), Negativo (25%)
     ```  
   - **Aprendizado**: A IA consegue detectar sentimentos mistos em uma única frase.

### 2. **Reconhecimento de Entidades (NER)**  
   - **Funcionalidade**: Extrair entidades como pessoas, locais, datas e organizações.  
   - **Exemplo de Saída**:  
     ```
     Texto: "Visitei a Microsoft em São Paulo em 2023."
     Entidades: 
       - "Microsoft" (Organização)
       - "São Paulo" (Local)
       - "2023" (Data)
     ```  
   - **Uso Prático**: Automatizar extração de dados de contratos ou e-mails.

### 3. **Extração de Frases-Chave**  
   - **Como Funciona**: Identifica termos relevantes para sumarização.  
   - **Caso de Uso**:  
     ```
     Texto: "O projeto foi concluído com sucesso, mas o orçamento excedeu em 10%."
     Frases-chave: "projeto concluído com sucesso", "orçamento excedeu em 10%"
     ```  

### 4. **CLU (Compreensão de Linguagem Personalizada)**  
   - **Treinamento de Modelos Customizados**:  
     - Criação de *intents* (ex: `SolicitarReembolso`).  
     - Definição de *entities* (ex: `DataVoo`, `NumeroPedido`).  
   - **Resultado**: Modelo capaz de classificar intenções em chatbots.  

### 5. **Resposta a Perguntas Personalizadas (Custom QA)**  
   - **Configuração**:  
     - Upload de documentos (PDF, URLs) para criar uma base de conhecimento.  
     - Teste direto no portal para validar respostas.  
   - **Exemplo**:  
     ```
     Pergunta: "Qual o prazo para devoluções?"
     Resposta: "O prazo máximo é de 30 dias após a compra."
     ```  
