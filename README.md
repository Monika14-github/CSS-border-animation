# CSS-border-animation
.......html.......
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width">
    <link href="style.css" rel="stylesheet" type="text/css" />
  </head>
  <div class="block"></block>
</html>
.......css........
body {
	margin: 0;
	padding: 0;
	background-color: black;
}

.block {
	position: relative;
	margin: 150px auto 0;
	width: 400px;
	height: 250px;
	background: linear-gradient(0deg, maroon, brown);
}

.block:before, .block:after {
	content: '';
	position: absolute;
	left: -2px;
	top: -2px;
	background: linear-gradient(45deg, aquamarine, turquoise, lime,chartreuse, yellow, indianred, 
		dodgerblue, cyan,#ffff00, violet);
	background-size: 400%;
	width: calc(100% + 4px);
	height: calc(100% + 4px);
	z-index: -1;
	animation: steam 20s linear infinite;
}

@keyframes steam {
	0% {
		background-position: 0 0;
	}
	50% {
		background-position: 400% 0;
	}
	100% {
		background-position: 0 0;
	}
}

.block:after {
	filter: blur(30px);
}
