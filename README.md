# GRID PERFORMANCE COMPONENT

An optimized Grid System for layout responsive websites

<code>CLASSES: {row, [xs- | lg-] _
          fit, fill, [1 | 6]}
</code>

row = with this class we start a gridblock of contents, everything inside this block gonna be affected by the .row class
      
      ex. <div class="row"> ... all elements inside get some grid default parameters ... </div>

[xs | lg] = @media-queries class, we pass grid parameters starting a class by one of this prefix (xs, sm, md, lg, xl) each class gonna affect just a specifici @media-queries size. <br>
          by default the main class who affect all the others @media-queries is the xs one <br>
          if definition class are missing all the grid taking xs default settings

          ex. <div class="row"> 
                <div class="sm-...></div>  <!-- xs will follows default rules cause xs it's undefined, sm, md, lg will follow defined custom parameters, sm-... parameters define by (min-width:...) all followed sizes but never previous sizes -->
                <div></div> <!-- cause parametrs affects also brothers of elements this div get some custom sm- rules -->
                <div></div> <!-- same for this -->
              </div>

grids parameters actually sets the main basic grid behavior: width through two variables (grow, content)<br>
   grow = take care to compare brothers same-media elements inside a defined block and output us a proportion through them that defined also the columns width.<br>
   content = affect width dimension of columns by the itself content (like an inline status)<br>

xs-[1 | 6] = set grows status<br>
xs-fit = set a content status<br>
xs-full = set a content status<br>

<pre>
             |             itself             |             childs             |       brothers     |
xs-[1 | 6]   |          grow: [1 | 6]         |          childs grow: 1        |   brothers grow: 1 |
xs-fit       |    grow: NO, content: inline   |    grow: NO, content: inline   |     NOT AFFECTED   |
xs-full      | grow: NO, entire space (block) | grow: NO, entire space (block) |     NOT AFFECTED   |
</pre>
