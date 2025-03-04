# Exercicio1
Trabalho!

1: Criando uma classe com private e métodos public
Crie uma classe Produto com os atributos nome e preco (ambos privados). Adicione métodos public para definir e obter os valores desses atributos. No programa principal, crie um objeto da classe e defina seus valores corretamente.
package exercicios;

public class Exercicio1 {
    public static void main(String[] args)      
      Produto p1 = new Produto("bolacha",2.54);
      Produto p2 = new Produto("cerveja");
      Produto p3 = new Produto();
           p1.Exibir();    
     p1.setNome();
     p1.setPreco(2.53);
     p1.Exibir();
                                 
    }
    
}

package exercicios;

public class Produto {
 
private String Nome;
private double Preco;


public Produto(){
    
}

public Produto(String Nome){
     this.Nome = Nome;
             
  }
public Produto(String Nome,double preco){
this.Nome = Nome;
this.Preco = preco;

}


 public void Exibir(){
    System.out.println("Nome:" + Nome);
    System.out.println("Preço:" + Preco);
}
 public String getNome(){
  return this.Nome;
  
  }
 
 public void setNome(){
   this.Nome = Nome;
 }
 
  public double getPreco(){
  return this.Preco;
  
 }
public void setPreco(double Preco){
     this.Preco = Preco;
  
 }
}

2 Validação de dados em métodos set
Modifique a classe Produto do exercício anterior para que o método setPreco(double preco) não permita valores negativos. Caso um valor inválido seja inserido, exiba uma mensagem de erro.
package exercicio2;

public class Produto {
 
private String Nome;
private double Preco;


public Produto(){
    
}

public Produto(String Nome){
     this.Nome = Nome;
             
  }
public Produto(String Nome,double preco){
this.Nome = Nome;
this.Preco = preco;

}


 public void Exibir(){
    System.out.println("Nome:" + Nome);
    System.out.println("Preço:" + Preco);
}
 public String getNome(){
  return this.Nome;
  
  }
 
 public void setNome(){
   this.Nome = Nome;
 }
 
  public double getPreco(){
  return this.Preco;
  
 }
public void setPreco(double Preco){
     this.Preco = Preco;
     
     if (Preco < 0){
         System.out.println("erro! o valor é menor do que o permitido.");
     } else {
    }

  
 }

}
package exercicios;

public class Exercicios {

    public static void main(String[] args) {
        
      Produto p1 = new Produto("bolacha",2.54);
      Produto p2 = new Produto("cerveja");
      Produto p3 = new Produto();
      
     p1.Exibir();
     
     p1.setNome();
     p1.setPreco(-2.53);
     p1.Exibir();
            
                
      
    }
    
}

3 Criando uma conta bancária com saldo protegido
Crie uma classe ContaBancaria com os atributos titular (público) e saldo (privado). Implemente métodos para depositar e sacar, garantindo que um saque não ocorra se o saldo for insuficiente. O método getSaldo() deve permitir acessar o saldo.
package exercicios;

public class ContaBancaria {

    public static void main(String[] args) {
    }

    // Atributo público para o titular da conta
    public String titular;

    // Atributo privado para o saldo da conta
    private double saldo;

    // Construtor para inicializar o titular e o saldo inicial
    public ContaBancaria(String titular, double saldoInicial) {
        this.titular = titular;
        this.saldo = saldoInicial;
    }

    // Método para depositar dinheiro na conta
    public void depositar(double valor) {
        if (valor > 0) {
            saldo += valor;
            System.out.println("Depósito de R$" + valor + " realizado com sucesso.");
        } else {
            System.out.println("Valor de depósito inválido.");
        }
    }

    // Método para sacar dinheiro da conta, garantindo saldo suficiente
    public void sacar(double valor) {
        if (valor <= saldo) {
            saldo -= valor;
            System.out.println("Saque de R$" + valor + " realizado com sucesso.");
        } else {
            System.out.println("Saldo insuficiente para o saque de R$" + valor);
        }
    }

    // Método para obter o saldo atual
    public double getSaldo() {
        return saldo;
    }
}

package exercicios;

public class Produto {

    private String nome;
    private double preco;

    // Construtor padrão
    public Produto() {
    }

    // Construtor com nome apenas
    public Produto(String nome) {
        this.nome = nome;
    }

    // Construtor com nome e preço
    public Produto(String nome, double preco) {
        this.nome = nome;
        this.preco = preco;
    }

    // Método para exibir detalhes do produto
    public void exibir() {
        System.out.println("Nome: " + nome);
        System.out.println("Preço: " + preco);
    }

    // Getters e Setters
    public String getNome() {
        return this.nome;
    }

    public void setNome(String nome) {
        this.nome = nome;
    }

    public double getPreco() {
        return this.preco;
    }

    public void setPreco(double preco) {
        if (preco < 0) {
            System.out.println("Erro! O valor é menor do que o permitido.");
        } else {
            this.preco = preco;
        }
    }
}

4 Uso de protected em uma hierarquia de classes
Crie uma classe Veiculo com um atributo protected chamado velocidadeMaxima. Depois, crie uma classe Carro que herde de Veiculo e adicione um método para exibir a velocidade máxima.
   
       // Construtor que chama o construtor da classe pai (Veiculo)
    public Carro(int velocidadeMaxima) {
        super(velocidadeMaxima); // Inicializa o atributo velocidadeMaxima da classe Veiculo
    }


    public void exibirVelocidadeMaxima() {
        System.out.println("A velocidade máxima do carro é: " + velocidadeMaxima + " km/h");
    }
}
  // Atributo protegido (protected) que pode ser acessado nas classes filhas
    protected int velocidadeMaxima;

    // Construtor
    public Veiculo(int velocidadeMaxima) {
        this.velocidadeMaxima = velocidadeMaxima;
   
    }
   } 

5 Criando uma classe Funcionario com private e public
Crie uma classe Funcionario com atributos privados nome e salario. Adicione métodos public para definir e obter esses valores. No programa principal, crie um objeto e exiba os dados.

    classe Funcionario
        Funcionario f1 = new Funcionario("João", 2500.50);
        Funcionario f2 = new Funcionario("Maria");

        // Exibindo os dados
        f1.exibir();
        f2.setSalario(3000.75);
        f2.exibir();

        // Alterando os dados de f1
        f1.setNome("Carlos");
        f1.setSalario(2700.25);
        f1.exibir();
    }
}

       // Atributos privados
    private String nome;
    private double salario;

    // Construtores
    public funcionario() {
    }

    public funcionario(String nome) {
        this.nome = nome;
    }

    public funcionario(String nome, double salario) {
        this.nome = nome;
        this.salario = salario;
    }

    // Métodos públicos para obter e definir os valores dos atributos
    public String getNome() {
        return this.nome;
    }

    public void setNome(String nome) {
        this.nome = nome;
    }

    public double getSalario() {
        return this.salario;
    }

    public void setSalario(double salario) {
        this.salario = salario;
    }

    // Método para exibir os dados do funcionário
    public void exibir() {
        System.out.println("Nome: " + nome);
        System.out.println("Salário: " + salario);
    }
}

6 Controle de acesso em uma classe de login
Crie uma classe Usuario com os atributos private login e senha. Adicione um método public boolean autenticar(String login, String senha) que verifica se os valores fornecidos correspondem aos armazenados.

   // Criando um usuário com login "admin" e senha "1234"
        Usuario usuario = new Usuario("admin", "1234");

        // Testando a autenticação
        if (usuario.autenticar("admin", "1234")) {
            System.out.println("Autenticação bem-sucedida!");
        } else {
            System.out.println("Autenticação falhou!");
        }

        // Testando a autenticação com dados incorretos
        if (usuario.autenticar("admin", "senhaErrada")) {
            System.out.println("Autenticação bem-sucedida!");
        } else {
            System.out.println("Autenticação falhou!");
        }
    }
}

public class Usuario {

    // Atributos privados
    private String login;
    private String senha;

    // Construtor
    public Usuario(String login, String senha) {
        this.login = login;
        this.senha = senha;
    }

    // Método para autenticar o usuário
    public boolean autenticar(String login, String senha) {
        // Verifica se o login e a senha fornecidos correspondem aos armazenados
        return this.login.equals(login) && this.senha.equals(senha);
    }
}

7 Subclasse acessando atributo protected
Crie uma classe Pessoa com um atributo protected chamado idade. Depois, crie uma classe Aluno que herde de Pessoa e crie um método que permita definir e exibir a idade do aluno.
package atividedes 7;

// Classe Pessoa
public class Pessoa {
    // Atributo protegido
    protected int idade;

    // Construtor
    public Pessoa(int idade) {
        this.idade = idade;
    }
}

// Classe Aluno que herda de Pessoa
public class Aluno extends Pessoa {
    
    private String login;
    private String senha;

    // Construtor
    public Aluno(int idade, String login, String senha) {
        super(idade);  // Chama o construtor da classe Pessoa
        this.login = login;
        this.senha = senha;
    }

    // Método para autenticar o usuário
    public boolean autenticar(String login, String senha) {
        // Verifica se o login e a senha fornecidos correspondem aos armazenados
        return this.login.equals(login) && this.senha.equals(senha);
    }

    // Método para definir a idade do aluno
    public void setIdade(int idade) {
        this.idade = idade;
    }

    // Método para exibir a idade do aluno
    public void exibirIdade() {
        System.out.println("Idade do aluno: " + this.idade + " anos");
    }

    // Testando a autenticação e exibição da idade
    public static void main(String[] args) {
        // Criando um aluno com login "admin", senha "1234" e idade 20
        Aluno aluno = new Aluno(20, "admin", "1234");

        // Testando a autenticação
        if (aluno.autenticar("admin", "1234")) {
            System.out.println("Autenticação bem-sucedida!");
            aluno.exibirIdade();  // Exibe a idade do aluno após autenticação
        } else {
            System.out.println("Autenticação falhou!");
        }
    }
package atividedes7;

public class Atividedes7 {

    public static void main(String[] args) {
 
            // Testando a autenticação
        if (aluno.autenticar("admin", "1234")) {
            System.out.println("Autenticação bem-sucedida!");
            aluno.exibirIdade();  // Exibe a idade do aluno após autenticação
        } else {
            System.out.println("Autenticação falhou!");
        }

        // Testando a autenticação com dados incorretos
        if (aluno.autenticar("admin", "senhaErrada")) {
            System.out.println("Autenticação bem-sucedida!");
        } else {
            System.out.println("Autenticação falhou!");
        }
    }
}

8 Criando um sistema de controle de acesso
Crie uma classe Porta com um atributo private boolean aberta. Adicione métodos public abrir() e fechar() para modificar o estado da porta, garantindo que nenhum código externo possa alterar diretamente esse estado.
8 Criando um sistema de controle de acesso
Crie uma classe Porta com um atributo private boolean aberta. Adicione métodos public abrir() e fechar() para modificar o estado da porta, garantindo que nenhum código externo possa alterar diretamente esse estado.
package exercicios;
public class Exercicio1 {
   public static void main(String[] args) { // Adicionado '{' na assinatura do main
       Produto p1 = new Produto("bolacha", 2.54);
       Produto p2 = new Produto("cerveja");
       Produto p3 = new Produto();
      
       p1.exibir();   
       p1.setNome("biscoito"); // Agora recebe um argumento
       p1.setPreco(2.53);
       p1.exibir();
      
       // Testando a classe Porta
       Porta porta = new Porta();
       porta.abrir();
       porta.fechar();
   }
}
package exercicio8;
public class Produto {
   private String nome; // Variáveis agora seguem a convenção de nomenclatura
   private double preco;
   public Produto() {
   }
   public Produto(String nome) {
       this.nome = nome;
   }
   public Produto(String nome, double preco) { // Corrigido para manter o padrão de nomes
       this.nome = nome;
       this.preco = preco;
   }
   public void exibir() { // Método renomeado para seguir convenção Java
       System.out.println("Nome: " + nome);
       System.out.println("Preço: " + preco);
   }
   public String getNome() {
       return this.nome;
   }
   public void setNome(String nome) { // Agora recebe um parâmetro
       this.nome = nome;
   }
   public double getPreco() {
       return this.preco;
   }
   public void setPreco(double preco) { // Parâmetro com nome correto
       this.preco = preco;
   }
}
package exercicios;
public class Porta {
   private boolean aberta; // Variável privada, não pode ser acessada diretamente
   public Porta() {
       this.aberta = false; // A porta começa fechada
   }
   public void abrir() {
       if (!aberta) {
           aberta = true;
           System.out.println("A porta foi aberta.");
       } else {
           System.out.println("A porta já está aberta.");
       }
   }
   public void fechar() {
       if (aberta) {
           aberta = false;
           System.out.println("A porta foi fechada.");
       } else {
           System.out.println("A porta já está fechada.");
       }
   }
   public boolean isAberta() { // Método para consultar o estado da porta
       return aberta;
   }
}


9 Implementando um protected método em uma classe base
Crie uma classe Animal com um método protected chamado fazerSom(). Depois, crie duas classes Cachorro e Gato que herdam de Animal e sobrescrevem esse método com sons diferentes. No programa principal, teste essas classes.

package exercicios;
// Classe Base
class Animal {
   protected void fazerSom() {
       System.out.println("O animal faz um som.");
   }
}
// Classe Cachorro herdando de Animal
class Cachorro extends Animal {
   @Override
   protected void fazerSom() {
       System.out.println("O cachorro late: Au Au!");
   }
}
// Classe Gato herdando de Animal
class Gato extends Animal {
   @Override
   protected void fazerSom() {
       System.out.println("O gato mia: Miau!");
   }
}
// Classe Principal (Main)
public class Exercicio9 {
   public static void main(String[] args) {
       Animal meuCachorro = new Cachorro();
       Animal meuGato = new Gato();
      
       meuCachorro.fazerSom(); // Saída: O cachorro late: Au Au!
       meuGato.fazerSom();      // Saída: O gato mia: Miau!
   }
}

10  Criando uma classe Carro com encapsulamento completo
Crie uma classe Carro com os atributos marca, modelo (privados) e ano (público). Implemente métodos getters e setters para os atributos privados e garanta que o ano do carro não possa ser menor que 1886 (ano do primeiro automóvel).

package exercicio10;
public class Carro {
   private String marca;
   private String modelo;
   public int ano; // Mantido público conforme solicitado
   // Construtor
   public Carro(String marca, String modelo, int ano) {
       this.marca = marca;
       this.modelo = modelo;
       setAno(ano); 
   }
   // Getter para marca
   public String getMarca() {
       return marca;
   }
   // Setter para marca
   public void setMarca(String marca) {
       this.marca = marca;
   }
   // Getter para modelo
   public String getModelo() {
       return modelo;
   }
   // Setter para modelo
   public void setModelo(String modelo) {
       this.modelo = modelo;
   }
   // Setter para ano
   public void setAno(int ano) {
       if (ano >= 1886) {
           this.ano = ano;
       } else {
           System.out.println("Erro: O ano do carro não pode ser menor que 1886!");
       }
   }
   // Método para exibir informações do carro
   public void exibirInfo() {
       System.out.println("Marca: " + marca);
       System.out.println("Modelo: " + modelo);
       System.out.println("Ano: " + ano);
   }
}
package exercicio10;
public class Exercicio10 {
   public static void main(String[] args) {
       Carro carro1 = new Carro("Toyota", "Corolla", 2020);
       carro1.exibirInfo();
       System.out.println("\nTentando definir um ano inválido...");
       carro1.setAno(1800); // Deve exibir uma mensagem de erro
      
       System.out.println("\nAlterando os dados...");
       carro1.setMarca("Honda");
       carro1.setModelo("Civic");
       carro1.setAno(2022);
       carro1.exibirInfo();
   }
}
