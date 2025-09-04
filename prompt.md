# Prompt para Análise e Melhoria do Projeto IMDB

## Objetivo
Analise todo o código do projeto, incluindo notebooks e arquivos Python, e faça as seguintes melhorias mantendo um estilo de escrita natural e humano, similar ao encontrado no notebook de EDA:

1. Antes de qualquer alteração, crie um backup completo do projeto usando:
```bash
cp -r /caminho/do/projeto /caminho/do/projeto_backup
```

2. Estrutura do Repositório:
   - Avalie a estrutura atual das pastas
   - Sugira e implemente melhorias na organização se necessário
   - Garanta que as pastas sigam as melhores práticas de um projeto de ciência de dados

3. Documentação:
   - Analise o README.md atual
   - Crie uma documentação clara e completa que inclua:
     * Descrição do projeto
     * Estrutura do repositório
     * Requisitos e dependências
     * Instruções de instalação e execução
     * Principais descobertas e conclusões
   
4. Revisão e Comentários do Código:
   - Analise cada notebook e arquivo Python
   - Adicione comentários explicativos mantendo um tom natural e didático
   - Mantenha o estilo de escrita similar ao encontrado no notebook de EDA
   - Exemplos de estilo:
     * "Essa análise mostra que filmes com alta participação do público tem avaliações mais altas."
     * "**Importante!:** Esta correlação não implica causalidade, pode haver viés de popularidade"
     * "Do ponto de vista prático, variações de 0.1-0.3 pontos na escala 0-10 não são relevantes"

5. Correção de Erros e Melhorias:
   - Identifique e corrija possíveis erros no código
   - Otimize trechos que podem ser melhorados
   - Sugira melhorias nas análises e visualizações
   - Mantenha a consistência do estilo em todo o projeto

6. Estrutura dos Notebooks:
   - Verifique se a sequência lógica está clara
   - Garanta que cada notebook tenha:
     * Título e objetivo claro
     * Seções bem definidas
     * Conclusões e próximos passos
     * Insights relevantes após cada análise

## Diretrizes de Estilo

1. Manter linguagem técnica mas acessível
2. Usar markdown para destacar pontos importantes
3. Incluir explicações dos conceitos quando relevante
4. Usar emojis com moderação e apenas quando apropriado
5. Manter um tom profissional mas não excessivamente formal

## Exemplos de Estilo de Escrita

### Comentários em Código
```python
# Calculamos a correlação entre as variáveis numéricas
# Note que usamos apenas as colunas relevantes para nossa análise
correlation_matrix = df[['IMDB_Rating', 'Meta_score', 'No_of_Votes']].corr()
```

### Insights e Análises
```markdown
**Insights da Análise:**
- Existe um claro "efeito diretor". Nomes como **Christopher Nolan** e **Quentin Tarantino** não apenas aparecem com frequência, mas mantêm uma nota média consistentemente alta.
- **Importante:** Com isso não é possivel afirmar que `Director` é um bom preditor para `IMDB_Rating`, esta análise mostra que a influência do diretor é mais forte em termos de consistência do que de excelência.
```

## Notas Importantes

1. Manter Consistência:
   - Use o mesmo estilo de formatação em todo o projeto
   - Mantenha o padrão de nomeação de variáveis e funções
   - Siga o mesmo fluxo lógico em todas as análises

2. Backup:
   - CRÍTICO: Sempre fazer backup antes de qualquer alteração
   - Manter uma cópia do projeto original para referência
   - Documentar todas as alterações feitas

3. Humanização:
   - Evitar linguagem muito robotizada ou formal
   - Manter um tom natural nas explicações
   - Usar exemplos práticos quando possível

## Estrutura Esperada do Projeto

```
LH_CD_LUCAS_DE_QUEIROS_SOUZA/
├── data/
│   ├── raw/              # Dados brutos
│   └── processed/        # Dados processados
├── models/              # Modelos treinados
├── notebooks/
│   ├── 01-tratamento_dos_dados.ipynb
│   ├── 02-eda.ipynb
│   └── 03-modelagem.ipynb
├── src/                 # Códigos fonte
├── README.md           # Documentação principal
└── requirements.txt    # Dependências do projeto
```

## Processo de Revisão

1. Fazer backup do projeto
2. Analisar estrutura atual
3. Revisar cada notebook sequencialmente
4. Documentar todas as alterações
5. Testar todas as células dos notebooks
6. Atualizar README.md
7. Verificar consistência geral do projeto

## Considerações Finais

- Manter o foco na clareza e qualidade do código
- Garantir que as análises sejam reproduzíveis
- Documentar decisões importantes
- Manter o estilo de escrita natural e didático
- Priorizar a legibilidade e manutenibilidade do código
