# dampbarn.github.io
Great repo
<!DOCTYPE html>
<html>
<head>
	<meta charset="utf-8">
	<title> Painful test</title>

	<style>
		body {
			font-family: sans-serif;
			width: 50%;
			max-width: 800px;
			min-width: 480px;
			margin: 0 auto;
		}
	</style>
</head>
<script>var rand = Math.ceil(Math.random() * 10);
var turns = 0;
var guess;

document.getElementById('button').addEventListener('click', guess);

function guess() {
    guess = document.getElementById('textbox').value;
    if (guess == rand) {
        alert('Correct! It took you ' + turns + ' turns to guess the number!');
    } else if (guess < rand) {
        alert('Your guess is to low. Try again.');
        turns++;
    } else if (guess > rand) {
        alert('Your guess is to high. Try again.');
        turns++;
    } else {
        alert('You didn\'t enter a number. Try again.');
    }
}

document.getElementById('reset').addEventListener('click', reset);

function reset() {
    rand = Math.ceil(Math.random() * 10);
    turns = 0;
    guess = null;
    document.getElementById('textbox').value = '';
    alert('The game has been reset!');
}
</script>
<body>
	<h1>Guess The Number</h1>
	<p>
		We have selected a random number
		between 1 - 10. See if you can
		guess it.
	</p>
