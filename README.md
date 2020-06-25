# CA_guessgame
Code Academy Guessing Game

let humanScore = 0;
let computerScore = 0;
let currentRoundNumber = 1;

// Write your code below:

function generateTarget(){
  return Math.floor(Math.random() * 9);
}

let compareGuesses = (human, computer, target) => {
    const userG = Math.abs(target - human);
    const computerG = Math.abs(target - computer);
    return userG <= computerG;

    /*if (userG <= computerG) {
        updateScore('human');
    } else {
        updateScore('computer');
    }*/
};

function updateScore(winner) {
  if(winner==="human"){
    humanScore +=1;
  }
  else {
    computerScore +=1;
  }
}

function advanceRound() {
  currentRoundNumber +=1;
}
