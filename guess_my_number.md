<div id="game">
    <p>Choose a number between 1-100</p>
    <p>Computer Guess</p>
    <p id="guess"></p>
    <button id="higher">Higher</button> <button id="lower">Lower</button>
</div>

<script>

document.addEventListener('load', function(e) {
    var game = document.querySelector('#game');
    var higher = document.querySelector('#higher');
    var lower = document.querySelector('#lower');
    var guess = document.querySelector('#guess');
    var ceiling = 100;
    var floor = 1;

   
    function guess_cpu() {
        cpu_guess = Math.floor(Math.random() * ceiling);
        guess.textContent = cpu_guess;
    }

    higher.addEventListener('click', function() {

    });

    lower.addEventListener('click', function() {

    });
    cpu_guess();
})
</script>