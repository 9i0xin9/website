# GRID PERFORMANCE COMPONENT

An optimized Grid System for layout responsive websites

CLASSES: {row, [xs|lg] 
          -fit, -fill, [-1|-6]}

row = with this class we start a gridblock of contents, everything inside this block gonna be affected by the .row class
      
      ex. <div class="row"> ... all elements inside get some grid default parameters ... </div>

[xs|lg] = @media-queries class, we pass grid parameters starting a class by one of this prefix (xs, sm, md, lg, xl) each class gonna take affection just to the specifici @media-queries size
          by default the main class who affect all the others @media-queries is the xs one
          if definition class are missing all the grid is taking xs default settings
          
          ex. <div class="row"> 
                <div class="sm-...></div>  <!-- xs will follows default rules cause xs it's undefined, sm, md, lg will follow           defined custom parameters, sm-... parameters define by (min-width:...) all followed sizes but never previous sizes -->
                <div></div> <!-- cause parametrs affects also brothers of elements this div get some custom sm- rules -->
                <div></div> <!-- same for this -->
              </div> 
                
               
                


