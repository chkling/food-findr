<!DOCTYPE html>
<html lang="en">
	<head>
		<meta charset="UTF-8" />
		<meta http-equiv="X-UA-Compatible" content="IE=edge" />
		<meta name="viewport" content="width=device-width, initial-scale=1.0" />
		<link rel="stylesheet" href="/stylesheets/home.css" />
		<link
			rel="stylesheet"
			href="../spice-restaurant-free-website-template/css/style.css"
		/>
		<link
			href="https://fonts.googleapis.com/icon?family=Material+Icons"
			rel="stylesheet"
		/>
		<link
			rel="stylesheet"
			href="../spice-restaurant-free-website-template/materialize/css/materialize.css"
			media="screen,projection"
		/>
		<link href="../spice-restaurant-free-website-template/css/bootstrap.min.css" rel="stylesheet" />
		<link href="../spice-restaurant-free-website-template/css/fancybox/jquery.fancybox.css" rel="stylesheet" />
		<link href="../spice-restaurant-free-website-template/css/flexslider.css" rel="stylesheet" />
		<link href="../spice-restaurant-free-website-template/css/style.css" rel="stylesheet" />
		<title>Home</title>
	</head>

    <body>
    <div id="wrapper" class="home-page">
    	<header>
    		<div class="navbar navbar-default navbar-static-top">
    			<div class="container">
    				<div class="navbar-header">
    					<button type="button" class="navbar-toggle" data-toggle="collapse" data-target=".navbar-collapse">
    						<span class="icon-bar"></span>
    						<span class="icon-bar"></span>
    						<span class="icon-bar"></span>
    					</button>
    					<a class="navbar-brand" href="/"><i class="icon-info-blocks material-icons">location_on</i>fo🍩d findr</a>
    				</div>
    				<div class="navbar-collapse collapse ">
    					<ul class="nav navbar-nav">
    						<li class="active"><a class="waves-effect waves-dark" href="/">Home</a></li>
    						<li><a class="waves-effect waves-dark" href="/reservations">Reservations</a></li>
    						<li><a class="waves-effect waves-dark" href="/logout">Sign Out</a></li>
    					</ul>
    				</div>
    			</div>
    		</div>
    	</header>
    		<section class="main-header">
    			<div class="container">
    				<div class="col-md-12">
    					<div class="aligncenter"><h2 class="aligncenter" id="find-food">Book reservations near you!</h2>
    						<a id="main-button" href="/reservations" type="button">FIND FOOD</a></div>
    			</div>
    		</div>
    		</section>
    		<div id="reservation-history">
    			<h3>Reservation History</h3>
    			<dl class="reservationcardcontainer">
    				${reservations.map(data => `
    				<div class="reservationcard">
    					<h4 class="name1">Restaurant</h4>
    					<dt class="dtcss">${data.Restaurant}</dt>
    					<h4 class="name2">Date</h4>
    					<dt class="dtcss">${data.Date}</dt>
    					<h4 class="name3">Time</h4>
    					<dt class="dtcss">${data.Time}</dt>
    					<h4 class="name4">Time</h4>
    					<dt class="dtcss">${data.Party_Size}</dt>
    					<button>Edit Reservation</button>
    					<button>Delete Reservation</button>
    				</div>
    				` ).join("")};

    			</dl>
                </div>

    </body>
    <script>

    	const reservationsFromDB = async (e) => {
    		const getReservations = await fetch("http://localhost:5321/reservations", {
    		method: "GET",
    		headers: {
    			"Content-Type": "application/json",
    		},
    		body: JSON.stringify(getReservations),
    	});

    };

    reservationsFromDB()

    	</script>

</html>
