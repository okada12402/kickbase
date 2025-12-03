let inning = 1;
let half = 'top'; // top=表, bottom=裏
let batter = 1; // 打者番号
let scores = { A: [0,0], B: [0,0] };
const maxInning = 2;

const scoreA1 = document.getElementById('scoreA1');
const scoreA2 = document.getElementById('scoreA2');
const scoreB1 = document.getElementById('scoreB1');
const scoreB2 = document.getElementById('scoreB2');
const totalA = document.getElementById('totalA');
const totalB = document.getElementById('totalB');
const batterDisplay = document.getElementById('batter');
const inningDisplay = document.getElementById('inning');
const winnerDisplay = document.getElementById('winner');

function updateDisplay() {
    scoreA1.textContent = scores.A[0];
    scoreA2.textContent = scores.A[1];
    scoreB1.textContent = scores.B[0];
    scoreB2.textContent = scores.B[1];
    totalA.textContent = scores.A.reduce((a,b)=>a+b,0);
    totalB.textContent = scores.B.reduce((a,b)=>a+b,0);
    batterDisplay.textContent = batter;
    inningDisplay.textContent = `${inning}回${half==='top'?'表':'裏'}`;
    
    if (inning > maxInning) {
        const totalScoreA = scores.A.reduce((a,b)=>a+b,0);
        const totalScoreB = scores.B.reduce((a,b)=>a+b,0);
        if (totalScoreA > totalScoreB) winnerDisplay.textContent = 'チームA勝利';
        else if (totalScoreB > totalScoreA) winnerDisplay.textContent = 'チームB勝利';
        else winnerDisplay.textContent = '引き分け';
    }
}

document.getElementById('addScore').addEventListener('click', ()=>{
    if (half === 'top') scores.A[inning-1]++;
    else scores.B[inning-1]++;
    updateDisplay();
});

document.getElementById('nextBatter').addEventListener('click', ()=>{
    batter++;
    // 例えば打者は1～9でループ
    if (batter > 9) {
        batter = 1;
        switchHalf();
    }
    updateDisplay();
});

function switchHalf() {
    half = (half==='top') ? 'bottom' : 'top';
    if (half === 'top') inning++;
}

updateDisplay();
