# jogo-herois
// Classe Heroi representando um personagem de aventura
class Heroi {
    constructor(nome, idade, tipo) {
        this.nome = nome;
        this.idade = idade;
        this.tipo = tipo.toLowerCase(); // padroniza para minúsculo
    }

    atacar() {
        let ataque;

        // Define o ataque de acordo com o tipo
        switch(this.tipo) {
            case "mago":
                ataque = "magia";
                break;
            case "guerreiro":
                ataque = "espada";
                break;
            case "monge":
                ataque = "artes marciais";
                break;
            case "ninja":
                ataque = "shuriken";
                break;
            default:
                ataque = "ataque desconhecido";
        }

        // Exibe a mensagem de ataque
        console.log(`${this.tipo} atacou usando ${ataque}`);
    }
}

// Exemplos de uso

const heroi1 = new Heroi("Gandalf", 150, "Mago");
const heroi2 = new Heroi("Aragorn", 87, "Guerreiro");
const heroi3 = new Heroi("Li Mei", 30, "Monge");
const heroi4 = new Heroi("Shinobi", 25, "Ninja");

heroi1.atacar(); // mago atacou usando magia
heroi2.atacar(); // guerreiro atacou usando espada
heroi3.atacar(); // monge atacou usando artes marciais
heroi4.atacar(); // ninja atacou usando shuriken
