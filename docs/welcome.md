class Animal {
    constructor(nome, idade, especie) {
        this.nome = nome;
        this.idade = idade;
        this.especie = especie;
    }

    printInfo() {
        console.log(`Nome: ${this.nome}, Idade: ${this.idade}, Espécie: ${this.especie}`);
    }
}

class Cachorro extends Animal {
    #raca;

    constructor(nome, idade, especie, raca) {
        super(nome, idade, especie);
        this.#raca = raca;
    }

    printInfo() {
        super.printInfo();
        console.log(`Raça: ${this.#raca}`);
    }
}

class Gato extends Animal {
    constructor(nome, idade, especie, cores) {
        super(nome, idade, especie);
        this.cores = cores;
    }

    printInfo() {
        super.printInfo();
        console.log(`Cores: ${this.cores.join(", ")}`);
    }
}

// Criando os objetos
let animal = new Animal("Simba", 3, "Leão");
let cachorro = new Cachorro("Rex", 5, "Cachorro", "Labrador");
let gato = new Gato("Jorge", 2, "Gato", ["branco", "preto"]);

// Imprimindo as informações
animal.printInfo();
cachorro.printInfo();
gato.printInfo();
