# AirflowPipeline para extração de Tweets via API
![This is an image](https://www.ambientelivre.com.br/media/k2/items/cache/f9a9b7c9f33a923e5475b478a62125ae_L.jpg) <br />
<br/>
Extrair os tweets e armazená-los, com isso a pessoa cientista de dados terá acesso aos dados e poderá traçar análises e modelos. <br />
<br/>
Algumas das soluções alternativas para a extração eventual dos dados seria por meio de um **Scheduler** que rodaria o código diariamente. O problema é que no dia em que o código não rodar por algum motivo, teremos um log? A pessoal responsável será informada? A cientista de dados conseguirá saber se está tudo bem com os dados? Se eles são confiáveis? Não garantimos isso com uma pessoa responsável, usando apenas um Scheduler. <br />
<br/>
Portanto, utilizar um **orquestrador de tarefas** como o apache Airflow que ajuda na resolução, justamente, desse tipo de problema: temos algumas tarefas para resolver no nosso pipeline de dados, isto é, no percurso que os nossos dados estão fazendo e podemos programá-lo para realizar essas tarefas, desde a extração de dados do twitter à disponibilização dos dados em um arquivo. Além disso, o Aiflow se ocupará de todos os problemas que levantamos até agora, por exemplo, gerar logs, adicionar tarefas no pipeline, ou rodar o código. Portanto, essa é uma ferramenta que foi pensada para o problema que estamos tentando resolver. <br />

## Data Pipeline e ETL
Data Pipeline é uma série de processos sucessivos que acontecem no processamento de dados. Por exemplo, podemos extrair os dados e armazená-los em um Data Lake ou Data Warehouse. Outra situação é pegar informações de um banco de dados e levar até uma aplicação financeira ou de outro tipo. Enfim, existem muitas possibilidades de trabalho com o data pipeline. <br/>
**ETL**: Extract, de extração; Transform, de transformação; e Load, de carregamento. O ELT é o processo de pegar os dados de uma fonte, fazer uma transformação neles e disponibilizá-los na etapa de Load. <br/>
<br/>
Apesar de os processo de data pipeline e ETL terem algumas semelhanças, o ETL faz parte de um data pipeline. Portanto, está inserido em um contexto de data pipeline, mas possui algumas etapas a mais que pode exercer. Por exemplo, é possível incluir uma etapa de machine learning, isto é, fazer transformações nos dados focadas no modelo de machine learning. O data pipeline consegue englobar a parte do ETL e trazer novas funções. Outra característica é o Batch de dados: Processamento de grandes volumes de dados. Por exemplo, no ETL, normalmente pegamos um pacote de dados, transformamos e disponibilizamos. Em um data pipeline, é possível que esse fluxo seja contínuo
