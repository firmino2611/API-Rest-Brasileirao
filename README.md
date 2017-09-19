<h1>API RestFul Campeonato Brasileiro de futebol</h1>
Documentação do meu projeto de TCC. <br>
API REST do Campeonato Brasileiro. <br>
Projeto em desenvolvimento, iniciado no dia 11/06/2017 <br>

<h2>Documentação em construção</h2>

Brasileirão Rest API
=========================

Rotas
-----

### Equipes ###
- /equipes > lista de equipes
- /equipes/{equipe} > info da equipe
- /equipes/{equipe}/escalacao > lista de jogadores
- /equipes/{equipe}/escalacao/{jogador> > info do jogador
- /equipes/{equipe}/jogos > lista de jogos
- /equipes/{equipe}/jogos/{jog}> > info do jogo
- /equipes/{equipe}/artilheiros > Lista de artilheiros do time

### Jogadores ###
- /jogadores > lista de jogadores
- /jogadores/{jogador} > info do jogador

### Jogos ###
- /jogos > lista de jogos
- /jogos/{jogo} > info do jogo
- /jogos/{data} > Lista de jogos que acontecerão na data

### Rodadas ###
- /rodadas > lista de rodadas
- /rodadas/{rodada} > info da rodada
- /rodadas/{rodada}/jogos > lista de jogos da rodada
- /rodadas/{rodada}/jogos/{jogo} > info do jogo da rodada

### Tabela ###
- /tabela > tabela

### Artilharia ###
- /artilharia > Lista de artilheiros

### Arbitragem ###
- /arbitragem > Lista de arbitros

### Cartões ###
- /cartao > Lista de jogadores com cartão
- /cartao/{jogador} > Lista de jogadores com cartão


Modelos
-------

### Equipes
* nome - str
* estado - str
* tecnico - str
* auxiliar - str
* medico - str
* preparador - str
* massagista - str
* jogadores - fk jogadores
* estado - str
* cidade - str
* fundacao - str

### Jogadores
* equipe - fk equipes
* nome - str
* apelido - str
* estado - str
* cidade - str
* idade - int
* posicao - str
* titular - bool
* profissional - bool
* amarelos - property
* vermelhos - property
* gols - property
* jogos - property

### Jogos
* mando - fk equipes
* visitante - fk equipes
* data - datetime
* estado - str
* cidade - str
* estadio - str
* rodada - int
* gols_pro_mando - property
* gols_pro_visitante - property
* gols_contra_mando - property
* gols_contra_visitante - property
* comissao = property
* arbitro = fk arbitros
* arbitro_assist_1 = fk arbitros
* arbitro_assist_2 = fk arbitros
* quarto_arbitro = fk arbitros

### Gols
* jogador = fk jogadores
* jogo = fk jogo
* time = time
* tempo = int
* contra = bol
* falta = bol
* penalti = bol

### Cartao
* jogador = fk jogadores
* jogo = fk jogo
* time = time
* tempo = int
* vermelho = bol
* amarelo = int

### Arbitros
* nome - str
* apelido - str
* estado - str
* cidade - str
* posicao - str

