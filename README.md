Dashboard Xbox Game Pass – Vendas de Assinaturas

Dashboard em Excel que acompanha o faturamento das assinaturas do Xbox Game Pass (2024), com filtros por tipo de assinatura e plano, indicadores, gráficos e as respostas das perguntas de negócio. Esta é a versão 2 (DASHBOARD_XBOX_v2.xlsx), refeita a partir da planilha original DASHBOARD_XBOX.xlsx.

Estrutura do projeto
projeto_xbox/
├── README.md
├── requirements.txt
├── build_dashboard.py        # gera o arquivo Excel
├── data/
│   └── DASHBOARD_XBOX.xlsx   # planilha original (fonte dos dados)
├── assets/                   # logos e avatar usados no dashboard
└── output/                   # o .xlsx gerado é salvo aqui
Abas do arquivo gerado
Aba	Conteúdo
Dashboard	Barra lateral com os filtros, 4 cards de indicadores, cards de EA Play e Minecraft e 4 gráficos.
Cálculos	Parâmetros, indicadores, tabelas dos gráficos, respostas das 4 perguntas de negócio e conferências.
Bases	Os dados (tabela tblAssinaturas).
Assets	Paleta de cores e logos.
Dados utilizados

Fonte: aba Bases da planilha original, com 295 assinaturas iniciadas entre 01/01/2024 e 16/12/2024. Não há valores ausentes nem IDs duplicados.

Coluna	Descrição
Subscriber ID, Name	Identificação do assinante
Plan	Core, Standard ou Ultimate
Start Date	Data de início da assinatura
Auto Renewal	Yes / No
Subscription Price	Preço do plano (Core 5, Standard 10, Ultimate 15)
Subscription Type	Monthly, Quarterly ou Annual
EA Play Season Pass / Price	Contratou (Yes/No) e valor (30)
Minecraft Season Pass / Price	Contratou (Yes/No) e valor (20)
Coupon Value	Desconto aplicado
Total Value	Subscription Price + EA Play Price + Minecraft Price − Coupon Value

Ajustes feitos nos dados em relação à planilha original:

Total Value passou de valor fixo para fórmula. Ela reproduz os 295 valores originais sem diferença.
O texto - na coluna de preço do EA Play virou 0 (exibido como "-").
Os cabeçalhos foram padronizados (sem quebra de linha).

Valores monetários estão em reais (R$). O faturamento total é R$ 7.633.

Perguntas de negócio

Respondidas na aba Cálculos e não dependem dos filtros:

Faturamento total dos planos anuais: R$ 1.754
Planos anuais por renovação automática: R$ 1.537 com e R$ 217 sem
Total de vendas de EA Play Season Pass: R$ 2.940
Total de vendas de Minecraft Season Pass: R$ 3.880
Como usar o dashboard
Abra DASHBOARD_XBOX_v2.xlsx no Excel (ou LibreOffice).
Na barra lateral verde, clique nas células brancas Tipo de assinatura e Plano e escolha um item da lista. Todos os indicadores e gráficos se atualizam.
Para atualizar os dados, cole novas linhas na aba Bases (as fórmulas leem até a linha 2000) e ajuste, na aba Cálculos, o ano de referência e a data de atualização (células em azul com fundo amarelo).
A barra lateral mostra "Todas as conferências OK" quando as somas por parte fecham com o total.
Como reproduzir (gerar o arquivo do zero)


