# tweeterpy_tweets_search
Extraia dados de tweets a partir da ferramenta de busca. Filtre por período, palavras-chave e aba e receba os dados em um arquivo csv.

### Ferramentas necessárias
Acima, existe um notebook nomeado como "twitter.ipybn". Ele necessita ser baixado na sua máquina, o que pode ser feito tanto através do Git quanto simplesmente clicando sobre ele e, na nova página carregada, clicando no botão "Download raw file" (ícone de seta para baixo). Este arquivo pode ser acessado através de Jupyter, ou seja, funciona através dos softwares Anaconda e Visual Studio Code. É primordial a instalação do Python na máquina, recomendo que em versão 3.10.

### Funcionalidades
No código, existem campos variáveis para que o usuário consiga filtrar as informações que ele precisa. Abaixo serão listadas as variáveis e para que servem.

"search_query": o usuário precisa digitar o texto que ele quer encontrar nos tweets. A ferramenta funciona como a barra de pesquisa do próprio Twitter, então seriam exatamente as mesmas palavras-chave de quando se pesquisa algum resultado na internet.

"total": faz-se uma limitação dos resultados que a API vai extrair. Caso o usuário queira extrair todos os resultados de um determinado intervalo de tempo, deverá deixá-la igual à None (total=None), que é considerado default da API.

"search_filter": filtra-se pela página de extração. Quando se olha a formatação do Twitter atual, existem as abas de pesquisa por Latest, Top, People, Photos e Videos (Product). O notebook está configurado como Latest, exibindo então os comentários ordenados do mais recente para o mais antigo. Caso o usuário queira alterar a visualização para enxergar os mais vistos, pode mudar a configuração como 'Top'.

"start_date" e "end_date": representam as datas de início e fim dos posts, respectivamente. Deve ser digitada no formato ano, mês e dia. Não é necessário do zero à esquerda para tornar meses ou dias com dois dígitos.

Quando o usuário clicar em "run" no notebook e alterar as variáveis necessárias, será salvo um arquivo csv contendo um ID do tweet, a data e horário da publicação e o texto do tweet. Está configurado para baixar um arquivo de nome "tweets.csv", mas o usuário também consegue alterar essa informação no notebook.

##### É importante frisar que esse csv vai estar na mesma pasta que o usuário deixou o notebook antes de abrí-lo (que, no geral, é em Downloads). Então é importante que se preste atenção em que diretório está o arquivo em python.

### Após a extração

O arquivo csv está configurado com o separador de "|". Após abrir o arquivo no Excel, selecione a primeira coluna inteira, clique na aba "Dados" e procure por "Texto para colunas". Selecione por "Delimitado", avance o processo e marque a caixa de seleção de "Outros", digitando a | no espaço em branco. Conclua o processo para que o texto esteja configurado em colunas, similar às tabelas.

##### Para verificar outras funcionalidades da API, acesse: https://github.com/iSarabjitDhiman/TweeterPy/tree/master
