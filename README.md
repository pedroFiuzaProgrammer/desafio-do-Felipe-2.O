function calcularNivel(vitorias, derrotas) {
    let saldo = vitorias - derrotas;
    let nivel;

    if (vitorias < 10) {
        nivel = "Ferro";
    } else if (vitorias >= 10 && vitorias <= 20) {
        nivel = "Bronze";
    } else if (vitorias >= 21 && vitorias <= 50) {
        nivel = "Prata";
    } else if (vitorias >= 51 && vitorias <= 80) {
        nivel = "Ouro";
    } else if (vitorias >= 81 && vitorias <= 90) {
        nivel = "Diamante";
    } else if (vitorias >= 91 && vitorias <= 100) {
        nivel = "Lendário";
    } else {
        nivel = "Imortal";
    }

    return { saldoVitorias: saldo, nivel: nivel };
}

// Exemplo de uso da função
const vitorias = parseInt(prompt("Digite a quantidade de vitórias: "));
const derrotas = parseInt(prompt("Digite a quantidade de derrotas: "));

const resultado = calcularNivel(vitorias, derrotas);

console.log(`O Herói tem um saldo de ${resultado.saldoVitorias} e está no nível de ${resultado.nivel}`);

