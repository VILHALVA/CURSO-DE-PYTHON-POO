# SINTAXE POO
POO (Programação Orientada a Objetos) é um paradigma de programação que se baseia na ideia de "objetos", que podem conter dados na forma de campos, também conhecidos como atributos, e código, na forma de procedimentos, geralmente chamados de métodos. Esses objetos são instâncias de classes, que funcionam como modelos para criar objetos.

Os quatro pilares da programação orientada a objetos são:

1. **Abstração:**
   - **Conceito:** Abstração é o processo de identificar características essenciais de um objeto e ignorar as características não essenciais. Em POO, uma classe é uma forma de abstração, pois representa um conjunto de objetos com características e comportamentos semelhantes.
   - **Exemplo de código:** Vamos criar uma classe `Veículo` que representa veículos em geral.

    ```python
    class Veiculo:
        def __init__(self, marca, modelo):
            self.marca = marca
            self.modelo = modelo
    
        def dirigir(self):
            print(f"Dirigindo o {self.modelo} da marca {self.marca}.")
    ```

2. **Encapsulamento:**
   - **Conceito:** Encapsulamento é o conceito de limitar o acesso direto aos atributos e métodos de um objeto e permitir o acesso apenas por meio de métodos específicos da classe. Isso ajuda a proteger os dados de manipulações não autorizadas.
   - **Exemplo de código:** Vamos adicionar um atributo privado à classe `Veiculo` e criar métodos para acessá-lo e modificá-lo.

    ```python
    class Veiculo:
        def __init__(self, marca, modelo):
            self.marca = marca
            self.modelo = modelo
            self.__ligado = False
    
        def ligar(self):
            self.__ligado = True
            print("Veículo ligado.")
    
        def desligar(self):
            self.__ligado = False
            print("Veículo desligado.")
    
        def esta_ligado(self):
            return self.__ligado
    ```

3. **Herança:**
   - **Conceito:** Herança é a capacidade de uma classe herdar atributos e métodos de outra classe. A classe que herda é chamada de classe derivada ou subclasse, enquanto a classe que é herdada é chamada de classe base ou superclasse.
   - **Exemplo de código:** Vamos criar uma classe `Carro` que herda de `Veiculo`.

    ```python
    class Carro(Veiculo):
        def __init__(self, marca, modelo, cor):
            super().__init__(marca, modelo)
            self.cor = cor
    
        def info(self):
            print(f"Marca: {self.marca}, Modelo: {self.modelo}, Cor: {self.cor}")
    ```

4. **Polimorfismo:**
   - **Conceito:** Polimorfismo é a capacidade de um objeto se comportar de maneiras diferentes, dependendo do contexto em que é usado. Em Python, isso é frequentemente implementado através da sobreposição de métodos em classes derivadas.
   - **Exemplo de código:** Vamos criar uma classe `VeiculoEletrico` que herda de `Veiculo` e sobrescreve o método `dirigir`.

    ```python
    class VeiculoEletrico(Veiculo):
        def __init__(self, marca, modelo, autonomia):
            super().__init__(marca, modelo)
            self.autonomia = autonomia
    
        def dirigir(self):
            print(f"Dirigindo o {self.modelo} da marca {self.marca} com autonomia de {self.autonomia} km.")
    ```

Estes são os quatro pilares da programação orientada a objetos, essenciais para entender como criar e trabalhar com objetos em Python (ou qualquer outra linguagem orientada a objetos).