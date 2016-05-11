# Hamburger icon menu
----

### Html syntax

- Option 1

		<header class="header">
			<div class= "header_inner">
				<a id="menu" class="header_menu">
					<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24">
		  			 	<path d="M2 6h20v3H2zm0 5h20v3H2zm0 5h20v3H2z"/>
					</svg>
				</a>
			</div>
		</header>
		<nav id="drawer" class="nav">
			<ul class="nav_list>
				<li class="nav_item"><a href="#">News</a></li>
				<li class="nav_item"><a href="#">Events</a></li>
				<li class="nav_item"><a href="#">Culture</a></li>
				<li class="nav_item"><a href="#">Blog</a></li>
			</ul>
		<nav>
	

- Option 2 
	
> After searching, reading, waiting I finally found an answer to my own question. Who wants to use an svg icon if png is a much better choice? Solution: [http://stackoverflow.com/questions/32903995/menu-icon-visible-in-chrome-but-not-in-androids-standard-browser](Menu icon visible in Android's browser")

**instead of**
	
	<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24">
    	<path d="M2 6h20v3H2zm0 5h20v3H2zm0 5h20v3H2z"/>
 	</svg>

**just use**

	<img src="/images/icon.png" height="32" width="32">


### CSS suntax
	
	@media screen and (max-width: 549px) {	
			.nav {
					z-index:10;
					background-color: #fff;
					width: 300px;
					position: absolute;
					/* This transform moves the drawer off canvas. */
					-webkit-transform: translate(-300px, 0);
					transform: translate(-300px, 0);
					/*Optional, we animate the drawer.*/
					transition:tranform 0.3s ease;
			}
		
			.nav.open {
						-webkit-transform: translate(0,0);
						transform: translate(0, 0);
			}
		
			.nav_item {
						display: list-items;
						border-bottom: 1px solid #E0E0E0;
						width: 100%;
						text-align: left;
			}
		
			.header_menu {
							display: inline-block;
							position: absolute;
							right: 0;
							padding: 1em;
			}
			
			.header_menu svg {
								width: 32px;
								fill: #000000;
			}
	}

### Other sources

[www.iconfinder.com](Iconfinder)				