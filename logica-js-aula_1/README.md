# guessing-game

# Jogo de Adivinhação de Números 🔢🎮

Um jogo em JavaScript para adivinhar um número secreto! 🎯  

---

## Como Jogar 🕹️

1. Abra o jogo e receba uma mensagem de boas-vindas. 🎉
2. Escolha um número entre **1 e 5000**. 🔢
3. Receba dicas se o número secreto é **maior** ou **menor** que o seu palpite. 🔍
4. Continue tentando até acertar! 🏆
5. Ao acertar, veja quantas tentativas você precisou. 🎉

---

## Código Principal 🛠️

```javascript
alert('Boas vindas ao jogo do número secreto');
let numeroMaximo = 5000;
let numeroSecreto = parseInt(Math.random() * numeroMaximo + 1);
let chute;
let tentativas = 1;

while (chute != numeroSecreto) {
    chute = prompt(`Escolha um número entre 1 e ${numeroMaximo}`);
    if (chute == numeroSecreto) {
        break;
    } else {
        alert(`O número secreto é ${chute > numeroSecreto ? 'menor' : 'maior'} que ${chute}`);
        tentativas++;
    }
}

let palavraTentativa = tentativas > 1 ? 'tentativas' : 'tentativa';
alert(`Isso ai! Você descobriu o número secreto ${numeroSecreto} com ${tentativas} ${palavraTentativa}.`);
