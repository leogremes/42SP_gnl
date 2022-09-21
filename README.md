<div><img src="https://game.42sp.org.br/static/assets/images/42-saopaulo.png" height=80>
<img src="https://game.42sp.org.br/static/assets/achievements/get_next_linee.png" align="right" height=100></div>

<br>

# GET_NEXT_LINE
Entregue em 28/06/2022

## Sobre

O objetivo deste projeto é criar uma função que aceite como parâmtro um número de <i>file descriptor</i>
e cada vez que for chamada retorne uma linha do conteúdo deste arquivo. O retorno deve ser um ponteiro
nulo em caso de arquivo inválido ou no caso de o arquivo já ter sido completamente lido.

### Exemplo:
Suponha que o seguinte arquivo esteja aberto no <i>file descriptor</i> 3

	Água mole em pedra dura
	Tanto bate até que fura

os retornos deveriam ser

	get_next_line(3)	// Água mole em pedra dura
	get_next_line(3)	// Tanto bate até que fura
	get_next_line(3)	// (null)

### Desenvolvimento
Para o desenvolvimento deste projeto deveríamos utilizar variáveis estáticas (que armazenam seu conteúdo até o fim do programa).
Essa variável foi utilizada em conjunto com outras funções que identificam a quebra de linha no conteúdo lido e separam
o que estava antes e depois dessa quebra, permitindo que não perdessemos o conteúdo já lido.

O projeto é composto por dois arquivos .c sendo um deles composto por funções auxiliares e outro pelas funções principais
e um arquivo .h contendo os protótipos das funções.
O bônus deste projeto consistia em ler vários arquivos ao mesmo tempo utilizando apenas uma variável estática e eu optei
por fazer utilizando listas encadeadas. Portanto, temos também os 3 arquivos do projeto bônus.


## Aprendizado
- <b>Variáves estáticas</b>
- Como <b>abrir e ler</b> arquivos (também editar)
- Reforço em <b>ponteiros</b> e <b>manipulação de strings</b>
- Identificação de <b><i>memory leaks</i></b>
