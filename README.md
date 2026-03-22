Nome: Livia da Silva Teixeira <br>
Matrícula: 2653161 <br>
Disciplina: Projeto de programação <br>
Professor: AMAURY NOGUEIRA NETO <br>
<br>

Por que Conta é abstrata? <br>
<p>
A classe Conta é abstrata porque representa uma ideia geral de conta.
Ela define atributos e métodos básicos (saldo, depósito, saque), mas não deve ser usada diretamente.
Quem realmente cria objetos são as classes filhas, como ContaCorrente e ContaPoupanca.
</p>
<br>

Por que Tributavel é interface? <br>
<p>
Tributavel é uma interface porque define uma regra:
toda classe que implementar precisa ter o método calcularTributo().
Isso permite que apenas algumas contas (como a conta corrente) paguem imposto, enquanto outras (como a poupança) não.
</p>
<br>

Como ocorre o polimorfismo no cálculo de imposto? <br>
<p>
O polimorfismo acontece quando o sistema trata diferentes objetos da mesma forma.
No método registrar(Tributavel t), ele aceita qualquer objeto que implemente a interface Tributavel.
</p>

<p>
No Banco, isso acontece quando o código percorre todas as contas e verifica quais são tributáveis:
</p>

<pre>
if (conta instanceof Tributavel) { //filtra se a conta implementa a interface(instanceof)
    calculadora.registrar((Tributavel) conta);
}
</pre>

<br>
Execução do sistema: <br>
<p>
O sistema pode ser executado abrindo o projeto em um editor Java (como IntelliJ ou Eclipse)
e rodando a classe Main.

Também é possível executar pelo terminal com os comandos:
</p>

<pre>
javac *.java
java Main
</pre>
<br>

Exemplo de Execução: <br> 
<pre> ===== BANCO JAVA =====
1 - Criar conta
2 - Listar contas
3 - Depositar
4 - Sacar
5 - Transferir
6 - Consultar saldo
7 - Calcular tributo de contas correntes
8 - Autenticar gerente
0 - Sair

Escolha uma opção: 2

Conta número: 0
Titular: Maria
Saldo: R$ 1000.0
---------------------

Conta número: 1
Titular: Rian
Saldo: R$ 6000.0
---------------------</pre>
