let  userscore = 0 ;
let  computerscore = 0 ;
const userscore_span = document.getElementById("user-score") ;
const computerscore_span = document.getElementById("computer-score") ;
const scoreboard_div = document.querySelector(".score-board") ;
const result_div = document.querySelector(".result > p");
const rock_div =  document.getElementById("rock") ;
const paper_div =  document.getElementById("paper") ;
const scissors_div =  document.getElementById("scissors") ;

function convertchoice (choice)
{
    if (choice === "r")
    {
	choice = "Rock" ;
    }
    else if (choice === "p")
    {
	choice = "Paper" ;
    }
    else {
	choice = "Scissors" ;
    }
    return choice ; 
}

function win (userchoice , computerchoice)
{
    userscore ++ ;
    userscore_span.innerHTML = userscore ;
    computerscore_span.innerHTML = computerscore ;
    result_div.innerHTML = convertchoice(userchoice) + " beats " + convertchoice(computerchoice) + " . YOU WIN " ; 
}

function lose (userchoice , computerchoice)
{
    computerscore ++ ;
    userscore_span.innerHTML = userscore ;
    computerscore_span.innerHTML = computerscore ;
    result_div.innerHTML = convertchoice(computerchoice) + " beats " + convertchoice(userchoice) + " . YOU LOSE " ; 
}

function draw ()
{
    result_div.innerHTML = "its a draw"
} 

function getcomputerchoice()
{
    const choices = ['r' , 'p' , 's'] ;
    randomnumber = Math.floor(Math.random() * 3) ;
    return choices[randomnumber] ; 
}

function game (userchoice) {
    const computerchoice = getcomputerchoice() ;
    console.log("user choice is : " + userchoice) ;
    console.log("computer choice is : " + computerchoice) ;
    const result = userchoice + computerchoice ;
    
    if (result === "rs" || result === "sp" || result === "pr" )
    {
	win(userchoice , computerchoice) ; 
    }
    else if (result === "sr" || result === "ps" || result === "rp")
    {
	lose(userchoice , computerchoice) ; 
    }
    else
    {
	draw(userchoice , computerchoice) ; 
    }
}

function main ()
{
    
rock_div.addEventListener('click' , function() {
    game("r") ; 
})

paper_div.addEventListener('click' , function() {
    game("p") ; 
})

scissors_div.addEventListener('click' , function() {
    game("s") ;
})
    
}

main () ; 
