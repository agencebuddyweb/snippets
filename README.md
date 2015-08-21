# Snippets
Collection of Buddyweb's finest snippets

## Javascript

### jQuery

#### Smooth Scroll

		$('.smooth-scroll').click( function() {
			var page = $(this).attr('href');
			var headerHeight = 80;
			var speed = 400; // Durée de l'animation (en ms)
			$('html, body').animate( { scrollTop: $(page).offset().top - headerHeight }, speed ); // On récupére l'espace perdu avec le header.
			return false;
		});
		
#### Faire un lien JS dans un élément HTML select

		<select id="dynamic_select">
		    <option value="" selected>Pick a Website</option>
		    <option value="http://www.google.com/">Google</option>
		    <option value="http://www.youtube.com/">YouTube</option>
		    <option value="http://www.stackoverflow.com/">Stack Overflow</option>
		</select>
		
		<script>
		    $(function(){
		      // bind change event to select
		      $('#dynamic_select').on('change', function () {
		          var url = $(this).val(); // get selected value
		          if (url) { // require a URL
		              window.location = url; // redirect
		          }
		          return false;
		      });
		    });
		</script>

