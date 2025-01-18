class Animal:
    def __init__(self, nombre, edad, especie):
        self.__nombre = nombre  # Encapsulación: atributo privado
        self.edad = edad
        self.especie = especie

    def hacer_ruido(self):
        print("¡El animal hace un sonido!")

    def get_nombre(self):
        return self.__nombre

class Perro(Animal):
    def __init__(self, nombre, edad, especie, raza, tamaño):
        super().__init__(nombre, edad, especie)
        self.raza = raza
        self.tamaño = tamaño

    def ladrar(self):
        print("¡Guau!")

class Gato(Animal):
    def __init__(self, nombre, edad, especie, color_ojos):
        super().__init__(nombre, edad, especie)
        self.color_ojos = color_ojos

    def maullar(self):
        print("Miau!")

# Creando objetos
perro1 = Perro("Firulais", 3, "Canino", "Labrador", "Mediano")
gato1 = Gato("Minino", 2, "Felino", "Verde")

# Demostrando polimorfismo
def hacer_sonar(animal):
    animal.hacer_ruido()

hacer_sonar(perro1)
hacer_sonar(gato1)
