# POO
POO
Suporte Para Poo (cap 12, Sebesta)

-Programação Orientada por Procedimentos:
*mais popular na decada de 70.
*subprogramas e bibiotecas.
*dados enviados a subprogramas para computação. Ex Classificação de um array de valores inteiros o vetor é enviado para um subprograma que o classifica.

-Programação Orientada a Objetos:
*Tem suas raizes de simula 87.
*Amplamente desenvolvida após a versão OO da Smaltalk (O.O. pura)
*Umas da linguagem OO deve oferecer
*Tipos de dados abtrastos(Classes)
*Herança
*Um tipo especial de vinculação dinâmica(Polimorfismo)

Orientação a objetos é um métodod de implementação no qual os subprogramas são organizados como um conjunto de objetos cooperantes, sendo cada objeto um representante de uma determinada classe, e as classes organizadas através de uma relação de herança.

-CLasses:
*Abstrações de objetos do mundo real.
*Cada classe deve respresentar um conceito
	Ex: Pessoa, veículo.
*Um conceito pode ser descrito por atributos
	Ex: 	Pessoa (Nome, data de nascimento, sexo)
		Veiculo(Marca, modelom tipo, ano, cor)
*Os atributos podem sofrer alterações(Operações)
*Leitura, escrita, atribuição, copia, adição...
*Dados + comportamento especificados no mesmo modulo (classes).
*Classes: Define um conjunto de objetos com a mesmas caracteristicas.
*Objetos são instancias de classes.

Elementos básicos de um programa OO
*Classes (atributos + metodos)
*Objetos: Variaveis dinâmicas criadas a partir de classes.
*Mensagens: Incação de metodos descritos na classe -> atuam sobre objetos.

Ex: Classe conta
	Atributos: Nome, Saldo
	Metodos: Depositar, Sacar, Consultar Saldo.
Os métodos são o protocolo de acesso aos atributos, e uma forma de modifica-los.

Obj 1			Obj 2
Nome Maria		Nome João
Saldo 1000,00		Slado 5.000,00

-Objeto:
*Cada objeto, quando instanciado, ocupa espaço de memória para seus dados.
*Cada objeto possui uma identidade.
*Cada objeto possui um tipo.
*Cada objeto possui variaveis e seus valores (Estado)
*Varios objetos podem ser criados apartir de uma mesma classe.

-Metodos
*Um método é uma abstração procedimental e sobre os dados é argumentos.
*São compartilhados entre todos objetos da classes.

-Mensagens
*Interface: COnjunto de serviços oferecidos por um objeto.
*Mensagem: Ativação de um metodo em um objeto.
*A interação entre objetos atraves se da a mensagem.
*Trocadads através da interface (ou Protocolo) especificado para o objeto pela sua classe.
*Cada mensagem é dirigida a um objeto e provoca a execução de um metodo sobre os dados particulares do objeto.

	Public Class Pessoa{
		Private String Nome;
		Private Int idade;
		Public Void exebir(){
			system.out.println(nome+"-"+idade);
	}
	Public pessoa(string, nome, int, idade){
		this.nome=nome;
		this.idade=idade;
	}}
	
	Public Class pragrama{
		Public static void main(String[] args){
			pessoa p1= new pessoa("Ana",30);
			pessoa p2= new pessoa("Lucas",18);
			p1.exebir();
			p2.exebir();}}
Saída:
	Ana-30
	Lucas-18

-Herança:
	Possui por obejtibo indentificar classes que possuem propriedades e comportamentos similares. Ex: Professor e uma pessoa, aluno é uma pessoa.
	A base da herança consiste no fato de que propriedades comuns (Gerais) são transmitidas a descentendes.
	Parte da POO consiste em estabelecer a hierarquia das classes.
	No caso mais simples, uma classe herda todas as entidades (variaveis e metodos) de sua classe pai mas isso pode ser evitado atraves dde controle de acesso.
	Herança Simples		Herança Multipla
-ùnuca classse pai		-N classes pai
-Arvore de derivação		-Grafo de derivação

		PAI
		Pessoa
		Nome
		DataNasc
	FILHOS
Professor		Aluno
Matricula		RA
Departamento		Curso
Classes derivadas ou subclasses.

	Além de herdar entidades de sua classe pai, uma classe derivada pode acrescentar novas entidades e modificar metodos herdados. Com o proposito de oferecer uma operação específica a objetos da classe derivada, mas que não seja apropriada para objetos da classes pai.

-Polimorfismo
	A classe pai pode definir um metodo que será sobreposto por suas classes.
	As operações definidas por tais metodos são similares, mas pode ser personalizados para cada classe da hierarquia, com isso, diferentes tipos de objetos podem responder a uma mesma mensagem de maneiras diferentes existem duas formas de polimorfismo.

*Redefinição (OverLone): Mesmo protocolo mas comportamentos diferentes - SObreposição.
*Sobrecarga(OverLoading): Mesmo nome de função mas diferentes parametros- Polimorfismo parametrico.

-Vinculação Dinamica
	Especialização + Polimorfismo
	Determinação de serviço chamado somente pode ser realizada em tempo de execução.
-Suporte para Poo em Java
	Java, como C++, não usa exclusivamente objetos somente valores de tipo exlares primitos não são objetos (Ex: Int, byte, float, char, double).
	Diferente de C++, Java não permite classes sem pai.
	Todas as classes devem ser subclasses da classe raiz.
	Object de algum descente de Object. Todos os objetos são alocados na memoria dinamica no monte (HEAP). A locação é feita com a opera por NEW não há operador de deslocação explicita.
	O coletor de lixo é responsável pela desalocação.

Pilha (Stack)		Monte(HEAP)

ii	Teste() int A= 10;
	Object A = New Object();
	Pessoa p1 = New Pessoa();
	Pessoa p2= p1
		if(p1.idade>18){
			pessoa.p3 = New pessoa();}
	A = NULL;
	Java suporta somente herança simples. Um metodo definido como final não pode ser sobreposto em nenhnuma classe descendente. Se a final é usado na especificação de uma classe, não pode ser extendidad por nenhum subclasse.

-Polimorfismo
	Em C++, um metodod deve ser definido como cirtual para permitir vinculação dinamica em Java todas as chamadas a metedos são vinculadas dinamicante, a menos que tenha definido como final, neste caso, ele não pode ser subreposto deixando todas as vinculações estaticas.

Subclasse herda				Subclasse não herda
Membros publicos e protegidos		membros privados
					construtores
membros sem modificador			metodos da mesma assinatura(redefine)
de acesso do mesmo pacote		variaveis de mesmo nome (esconde)

-Conceitos basicos da linguagens Java
	Java é uma plataforma de desenvolvimento muito capaz de produzir softwares para diversos tipos de disposistivos é uma tecnologia composta de cada arquivo de código fonte Java pode conter varias classes, mas somente uma publica, com o mesmo nome do arquivo, tudo em Java deve estar, dentro de classes com o metodo main fornecem um ponto de inicio de execução de um programa Java invocada pela JVM

-Programação em Java
*Linguagem de programação (sintaxe)- Impretativa, estruturada, O.O.
*Dada Api, conjunto de classes já implementadas ultilizadas essencialmente por todo programa Java(Ex Object), ou ultilizadas (ex. Int)

	A programação em Java SE baseia na codificação de classes. Classe base: Object uma classe é definida em termos de

*Pacote				Tipos de Dados
*Nome				Boolean	True/False
*SuperClasses			Byte	128 a 127
*Interfaces			Char	0 a 65535(ASCII)
*Construtores			Sdect	21k a 21k
*Atributos			int	32bits
*Metodos			long	64bits
				float	32bits(real)
				double	64bits(real)
*Fortemente tipada
*Metodos devem retornar algum valor, ou Void.
*Passagem de parametros sempre por valor.
	O Java trabalha com conceito de pacotes, cada pacote e um diretorno de codigo  fonte, o nome completo (canoco) de uma lasse é o nome do pactoe seguida do nome da classe. Ex: Java.lanc_object) para utilizar classe de outros pacotes é possivel importalas(import)

-Abstrações:
	Um metodo abstrato não poussir corpo. Sua implentação fica a cargo de classes pilhas(polimorfismo). Metodos abtrasto devem estar em classes abstratas, uma classe abstrata não pode ser instanciada(new)
	Interfaces são clases 100% abstratas
Public absctract class pessoa`
	String nome;
Public abstract Void apresentar ();}
Public Class aluno externos pessoa{
Public void apresentador(){
	systeam.out.println("nome");}
Public Static Void Main(string[]args){
	Pessoa P= New aluno();
	P.apresenta();}}

-Java SE x Java EE
	A especifacaão Java SE é implementada pela JVM.
	A especificação Java EE é implentada pelos servidores de aplicação e (ou por bibliotecas de escrever) Servidores de aplicação "rodam" sobre a JVM.
	Uma aplicação Java EE (web, por exemplo) "Roda" sobre um servidor de aplicação - 10c indesion of control

Especificação (API)				Implementação
Foto

