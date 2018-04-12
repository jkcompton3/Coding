<html>
<head>
<link href="MrC_Form.css" rel="stylesheet" />
</head>

<body>
	<form name="MovieQuiz">
    	<fieldset>
        <legend>Mr. C's Movie Quiz</legend>
        <div>
        	<fieldset>
            <legend>Question #1</legend>
        	<p>Who is the lead character in "Black Panther?"</p>
            <input type="radio" name="q1" value="chewy"/> Chewy
            <br />
            <input type="radio" name="q1" value="tchala"/> T'chala
            <br />
            <input type="radio" name="q1" value="killmonger"/> Killmonger
            <br />
            <input type="radio" name="q1" value="eric"/> Eric
            </fieldset>
        </div>
        <div>
        	<fieldset>
            <legend>Question #2</legend>
        	<p>Which movies feature Tom Hanks?</p>
            <input type="checkbox" name="q2a" value="Big"/> Big
            <br />
            <input type="checkbox" name="q2b" value="Mission Impossible"/> Mission Impossible
            <br />
            <input type="checkbox" name="q2c" /> Shawshank Redemption
            <br />
            <input type="checkbox" name="q2d" /> Cloud Atlas
            <br />
            <input type="checkbox" name="q2e" /> Star Wars
            <br />
            <input type="checkbox" name="q2f" /> Castaway
            <br />
            <input type="checkbox" name="q2g" /> The Green Mile
            </fieldset>
        </div>
        <div>
        <fieldset>
            <legend>Question #3</legend>
        	<p>Which character is not related to Luke Skywalker?</p>
            <select name="q3">
            	<option value="Leia"> Leia </option>
                <option value="Darth Vader"> Darth Vader </option>
                <option value="Chewy">Chewy</option>
                <option value="Padme">Padme</option>
            </select>
        </fieldset>
        </div>
        <div>
        <fieldset>
            <legend>Question #4</legend>
        	<p>What is the name of the Nazi-fighting archaelogist played by Harrison Ford?</p>
            <input name="q4" type="text" placeholder="Answer here" />
        </fieldset>
        </div>
        <div>
        <fieldset>
            <legend>Question #5</legend>
        	<p>Name this movie: "The Hunt for <input name="q5" type="color"/> October"</p>
            
        </fieldset> 
        </div>
        <div>
        <fieldset>
            <legend>Question #6</legend>
        	<p>In "Legally Blonde," what career does she pursue?</p>
            <input type="button" value="Janitor" onclick="answerJ()"/>
            <input type="button" value="Teacher" onclick="answerT()"/>
            <input type="button" value="Professional Shopper" onclick="answerP()"/>
            <input type="button" value="Lawyer" onclick="answerL()"/>
        </fieldset>
        </div>
        <div>
        	<p>Thanks for playing!</p>
        	<input type="submit" onclick="answerChecker()"/>
        </div>
        </fieldset>
    </form>
    <script>
	function answerChecker() {
//checks which radio button is selected
		if(document.MovieQuiz.q1.value==="tchala") {
			alert("Question 1 is correct!");
		} else {
			alert("Question 1 WRONG!");
		}
//checks which checkboxes are clicked - only says correct if ALL BOXES are correct!
		if(document.MovieQuiz.q2a.checked===true && document.MovieQuiz.q2d.checked===true && document.MovieQuiz.q2f.checked===true && document.MovieQuiz.q2g.checked===true && document.MovieQuiz.q2b.checked===false && document.MovieQuiz.q2c.checked===false && document.MovieQuiz.q2e.checked===false) {
			alert("Tom Hanks WAS in all those! Nice work on question 2!");
		} else {
			alert("Nope. Better check IMDB and come back to question 2.");
		}
//checks which option is chosen on select menu
		if(document.MovieQuiz.q3.value==="Chewy") {
			alert("You really know your Star Wars. Yes to question 3.");
		} else {
			alert("No. It was Chewy for question 3.");
		}
//checks what is typed into textbox on question 4
		if(document.MovieQuiz.q4.value==="Indiana Jones") {
			alert("Question 4 is correct!");
		} else {
			alert("Nope on Question 4");
		}
//checks which color was selected on the color picker
		if(document.MovieQuiz.q5.value==="#ff0000") {
			alert("Red October! Correct on question 5!");
		} else {
			alert("No, it's not Green October. Question 5 wrong.");
		}
	}
//answerChecker ends above
	function answerJ(){
		alert("No");
	}
	function answerT(){
		alert("Not at all");
	}
	function answerP(){
		alert("Nope");
	}
	function answerL(){
		alert("YES! You got it!");
	}
	</script>
</body>











</html>
