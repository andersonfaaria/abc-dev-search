# Startup de Tecnologia na região do ABC

## Perpectiva do negócio

Um grupo de empreendedores querem abrir uma startup de tecnologia na região do ABC. Para tal precisam de informações sobre os profissionais que residem na área, para averiguar se é viável abrir um escritório na região.

## Objetivos

* Verficar a existência de profissionais qualificados residentes na região;
* Verificar as condições de trabalho (salário, distância do trabalho atual, situação de moradia) destes profissionais.

## Campos selecionados e justificativas (Macro)

* Dados residenciais
* Idade
* Informações acadêmicas
* Informações trabalhistas
  * Salário
  * Área de atuação
  * Local de trabalho
  * Tempo de deslocamento entre casa e trabalho

### Campos de acordo com o documento do censo

* UNIDADE DA FEDERAÇÃO
* CÓDIGO DO MUNICÍPIO
* REGIÃO GEOGRÁFICA
* CÓDIGO DA MESORREGIÃO
* CÓDIGO DA MICRORREGIÃO
* CÓDIGO DA REGIÃO METROPOLITANA
* SITUAÇÃO DO DOMICÍLIO
* SEXO
* VARIÁVEL AUXILIAR DA IDADE CALCULADA (ANOS E MESES)
* TEMPO DE MORADIA NA UF
* TEMPO DE MORADIA NO MUNICÍPIO
* UF DE RESIDÊNCIA ANTERIOR
* MUNICÍPIO DE RESIDÊNCIA ANTERIOR
* CURSO QUE FREQUENTA
* SÉRIE / ANO QUE FREQUENTA
* SÉRIE QUE FREQUENTA
* CONCLUSÃO DE OUTRO CURSO SUPERIOR DE GRADUAÇÃO
* CURSO MAIS ELEVADO QUE FREQUENTOU
* CONCLUSÃO DESTE CURSO
* ESPÉCIE DO CURSO MAIS ELEVADO CONCLUÍDO
* NÍVEL DE INSTRUÇÃO
* CURSO SUPERIOR DE GRADUAÇÃO
* CURSO DE MESTRADO
* CURSO DE DOUTORADO
* MUNICÍPIO E UNIDADE DA FEDERAÇÃO OU PAÍS ESTRANGEIRO QUE FREQUENTAVA ESCOLA (OU CRECHE)
* UF QUE FREQUENTAVA ESCOLA (OU CRECHE)
* MUNICÍPIO QUE FREQUENTAVA ESCOLA (OU CRECHE)
* PAÍS ESTRANGEIRO QUE FREQUENTAVA ESCOLA (OU CRECHE)
* VIVE EM COMPANHIA DE CÔNJUGE OU COMPANHEIRO(A)
* NATUREZA DA UNIÃO
* ESTADO CIVIL
* QUANTOS TRABALHOS TINHA
* OCUPAÇÃO
* ATIVIDADE
* NESSE TRABALHO ERA
* QUANTAS PESSOAS EMPREGAVA NESSE TRABALHO
* NO TRABALHO PRINCIPAL, QUAL ERA O RENDIMENTO BRUTO (OU A RETIRADA) MENSAL QUE GANHAVA HABITUALMENTE * EM JULHO DE 2010
* VALOR DO RENDIMENTO BRUTO (OU A RETIRADA) MENSAL NO TRABALHO PRINCIPAL
* RENDIMENTO NO TRABALHO PRINCIPAL
* VALOR DO RENDIMENTO BRUTO (OU A RETIRADA) MENSAL NOS DEMAIS TRABALHOS (EM REAIS)
* RENDIMENTO EM TODOS OS TRABALHOS
* RENDIMENTO EM TODOS OS TRABALHOS EM Nº DE SALÁRIOS MÍNIMOS
* EM QUE MUNICÍPIO E UNIDADE DA FEDERAÇÃO OU PAÍS ESTRANGEIRO TRABALHA
* EM QUE UNIDADE DA FEDERAÇÃO TRABALHAVA
* EM QUE MUNICÍPIO TRABALHAVA
* EM QUE PAÍS ESTRANGEIRO TRABALHAVA
* RETORNA DO TRABALHO PARA CASA DIARIAMENTE
* QUAL É O TEMPO HABITUAL GASTO DE DESLOCAMENTO DE SUA CASA ATÉ O TRABALHO

### Tabelas auxiliares utilizadas

* Cursos Doutorado_Estrutura 2010.xls;
* Cursos Mestrado_Estrutura 2010.xls;
* Cursos Superiores_Estrutura 2010.xls;
* Estrutura atividade CD2000.xls;
* Ocupação COD 2010.xls;
* Unidades da Federação, Mesorregiões, microrregiões e municípios 2010.xls.

## Desenvolvimento

### Staging Area

Foi utilizado a ferramenta de ETL da Microsoft (SSDT) para a construção da Staging Area.

Dados da tabela de informações pessoais:

![alt text](/staging_area.png "Staging Area")

Lista de tabelas da Staging Area:

![alt text](/staging_area_02.png "Tabelas da Staging Area")

#### ETL

Os pacotes de importação foram divididos em:

* Importar Dados Pessoais;
* Importar Regiões;
* Importar Cursos Superiores;
* Importar Cursos de Doutorado;
* Importar Cursos de Mestrado;
* Importar Ocupação;
* Importar Atividades.

Pacotes ETL:

![alt text](/etl_staging_area_01.png "Pacotes do ETL")

Pacote "Importar Dados Pessoais":

![alt text](/etl_staging_area_02.png "Importar Dados Pessoais")

Demais pacotes de importação:

![alt text](/etl_staging_area_03.png "Demais passos de importação")