# Progrma-Orientada-a-Objeto

Polimorfismo:
O polimorfismo é um princípio da programação orientada a objetos que permite que objetos de diferentes classes sejam tratados de forma uniforme, desde que implementem uma mesma interface ou herdem de uma mesma classe base. O polimorfismo permite que um objeto seja referenciado por meio de um tipo genérico, mas a implementação específica do método chamado será determinada em tempo de execução, dependendo do tipo real do objeto.

python (polimorfismo)

class Animal:
    def fazer_som(self):
        pass

class Cachorro(Animal):
    def fazer_som(self):
        print("Au Au!")
        

class Gato(Animal):
    def fazer_som(self):
        print("Miau!")

def emitir_som(animal):
    animal.fazer_som()

cachorro = Cachorro()
gato = Gato()

emitir_som(cachorro)  # Saída: Au Au!
emitir_som(gato)  # Saída: Miau!


#Nesse exemplo, temos uma classe base chamada Animal que possui um método fazer_som(), que é definido como uma operação genérica e não 
#implementada. Em seguida, temos duas classes derivadas, Cachorro e Gato, que herdam da classe Animal e implementam o método fazer_som()
#de acordo com o som específico que cada animal faz.

#A função emitir_som(animal) recebe um objeto do tipo Animal como argumento e chama o método fazer_som(). O polimorfismo ocorre quando 
#chamamos emitir_som(cachorro) e emitir_som(gato). Apesar de chamarmos o mesmo método em objetos de classes 
#diferentes, o comportamento do método é determinado pelo tipo real do objeto em tempo de execução, 
#resultando na impressão do som específico de cada animal.
