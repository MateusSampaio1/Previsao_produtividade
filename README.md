# Previsao_produtividade
 Previsão da produtividade de funcionários do segmento têxtil, mais específicamente da indústria de vestuário.

# Contextualização.
O segmento têxil e de vestuário é um dos segmentos industriais mais importantes no mundo globalizado e o Brasil encontra-se entre os maiores players deste mercado. O intuito deste projeto é utilizar um algorítmo capaz de realizar uma regressão linear, visando prever a produtividade de funcionários que trabalham neste setor.

# Informações sobre o projeto
O dataset utilizado pode ser encontrado no [Kaggle](https://www.kaggle.com/datasets/ishadss/productivity-prediction-of-garment-employees) e contêm algumas caracteristicas como departamento, time, a produtividade desejada, tempo ocioso da produção, dentre outras. Abaixo seguem uma breve descrição das colunas:

- **Date**: Data no formato Mês - Dia - Ano;
- **Quarter**: Uma fração do mês (Mês/3);
- **Department**: O departamento;
- **Day**: Dia que o dado foi coletado;
- **Team**: Número associado ao time;
- **Targeted_productivity**: Produtividade desejada;
- **Smv**: Tempo alocado para cada tarefa (padrão);
- **Wip**: Trabalho em desenvolvimento, inclui a qtd de itens inacabados p/ produto;
- **Over_time**: Horas extras de cada equipe;
- **Incentive**: Valor do incentivo financeiro (em BDT);
- **Idle_time**: Tempo ocioso (produção parada por qualquer motivo);
- **Idle_men**: Qtd de trabalhadores que ficarão ociosos devido a parada na produção;
- **No_of_style_change**: Número de mudanças no estilo de um determinado produto;
- **No_of_workers**: Número de trabalhadores por equipe;
- **Actual_productivity**: Produtividade alcançada.

Neste projeto foram utilizadas a bibliotecas [Pandas](https://pandas.pydata.org/docs/), [Seaborn](https://seaborn.pydata.org/), [Numpy](https://numpy.org/doc/stable/), [Scikit Learn](https://scikit-learn.org/stable/) e [XGBoost](https://xgboost.readthedocs.io/en/stable/python/python_api.html#xgboost.Booster.predict).

O algorítimo que apresentou um melhor desempenho, dentre os testados neste projeto, foi o **XGBRegressor**. Conseguindo alcançar uma raiz do erro quadrático médio(**RMSE**) de 0.1255 e um erro absoluto(**MAE**) de 0.0757, após a otimização. 