# colors
week 2 assignment
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="utf-8">
    <meta name="generator" content="CoffeeCup HTML Editor (www.coffeecup.com)">
    <meta name="dcterms.created" content="Sun, 24 Apr 2016 00:01:44 GMT">
    <meta name="description" content="">
    <meta name="keywords" content="">
    <title></title>
    
    <!--[if IE]>
    <script src="http://html5shim.googlecode.com/svn/trunk/html5.js"></script>
    <![endif]-->
	<script>
	function do_game(){
			 var colors = ["aqua","beige","black","cyan","gold","green","maroon","olive","orange","teal","white","yellow"];
			 var target_index = ((Math.random())*(colors.length));
			 var target_index_int=Math.floor(target_index);
			 var finished=false;
			 guesses=0;
			 var target = colors[target_index_int];
			   
		
			 while(!finished){ 
			 var guess_input_text = prompt("I am thinking of one of these colors:\n\n"+
			 "aqua,beige,black,cyan,gold,green,maroon,olive,orange,teal,white,yellow\n\n"+
			 "What color am I thinking of?");
			 guesses+=1;
			 finished=check_guess();
			 }
			 
			 function check_guess(){
			 if (colors.indexOf(guess_input_text)==-1)
			 {
			 alert("Sorry! I do not recognize your color.\n\n"+
			 "Please try again!");
			 return false;
			 }
			 else
			 if (guess_input_text > target){
			 alert("Sorry! Your guess is not correct.\n\n"+
			 "Hint: Your color is alphabetically higher than mine.\n\n"+
			 "Please try again!");
			 return false;
			 }
			 else
			 if (guess_input_text < target){
			 alert("Sorry! Your guess is not correct.\n\n"+
			 "Hint: Your color is alphabetically lower than mine.\n\n"+
			 "Please try again!");
			 return false;
			 }
			 else
			 if (guess_input_text == target){
			 alert("Congratulations! You have guessed the color.\n\n"+
			 "It took you "+guesses+ " guesses to finish the game.\n\n"+
			 "You can see the color in the background.");
			 return true;
			 }
	}
myBody=document.getElementsByTagName("body")[0];


myBody.style.background=target;	
	}
	</script>
	
  </head>
  <body onload="do_game()">

  </body>
</html>
