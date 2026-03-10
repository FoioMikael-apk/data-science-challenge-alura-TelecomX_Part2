📊 Desafio Telecom X: Análise de Churn e Machine Learning
Fala pessoal! Este é o repositório do meu projeto para o Desafio Telecom X, desenvolvido como parte da formação em Data Science do Oracle Next Education (ONE) em parceria com a Alura.

A ideia deste desafio foi colocar a mão na massa para resolver um problema super comum no mercado: o Customer Churn (evasão de clientes). Peguei uma base de dados bruta, fiz todo o processo de ETL, analisei os motivos dos cancelamentos e, por fim, treinei um modelo de Inteligência Artificial para prever quais clientes têm maior risco de ir embora.

🛠️ Ferramentas que usei
Python (Linguagem principal)

Pandas (Para extração, limpeza e manipulação dos dados)

Scikit-Learn (Para a criação do modelo preditivo de Machine Learning)

Matplotlib & Seaborn (Para a criação dos gráficos)

Jupyter Notebook / Google Colab (Ambiente de desenvolvimento)

🚀 Como o projeto foi construído (Passo a Passo)
1. ETL (O pesadelo do JSON aninhado)
Os dados vieram em um arquivo JSON (TelecomX_Data.json), mas as informações financeiras e de serviços estavam "escondidas" em dicionários dentro das colunas. Para resolver isso, usei a função pd.json_normalize do Pandas, que "achatou" os dados e transformou tudo em uma tabela estruturada. Depois, padronizei o nome das colunas e tratei os valores vazios na coluna de gastos totais forçando a conversão numérica com o coerce.

2. Análise Exploratória de Dados (EDA)
Com a base limpa, criei alguns gráficos para cruzar o cancelamento (Churn) com o perfil do cliente. As principais descobertas foram:

A armadilha do Cheque Eletrônico: A esmagadora maioria dos cancelamentos acontece com clientes que usam o "Electronic Check" como pagamento. Quem usa métodos automáticos (cartão/débito) é muito mais fiel.

Preço do plano: Clientes pagando mensalidades mais altas (próximas a $80) cancelam muito mais do que a galera dos planos básicos (abaixo de $65).

3. Machine Learning (Prevendo o futuro)
Para fechar o projeto, preparei os dados transformando textos em números usando One-Hot Encoding (pd.get_dummies) e treinei um modelo preditivo usando o algoritmo Random Forest.

Resultado: O modelo atingiu uma acurácia geral de 79%.

Valor de negócio: Mesmo com uma base de dados desbalanceada, o modelo consegue identificar com precisão uma boa parcela dos clientes prestes a cancelar. Isso permitiria que a equipe de retenção parasse de atirar no escuro e oferecesse descontos focados apenas nos clientes com risco real de evasão.

💻 Como testar o projeto na sua máquina
Faça o clone deste repositório.

Certifique-se de ter as bibliotecas instaladas (pip install pandas scikit-learn matplotlib seaborn).

Abra o arquivo TelecomX_BR_Finalizado.ipynb no Jupyter Notebook ou faça o upload no Google Colab.

Rode as células sequencialmente (o arquivo TelecomX_Data.json precisa estar na mesma pasta).
