use this scss to make classes for each of your sprites from a sprite map.

in your main.scss   `@import "{}/imports/ui/scss/sprites";`

and then create your classes with something like:
`@include divide_sprite_map('good_guys', 'sprites_by_demonhuntrpg_transparent.png', 32px, 32px, 4 , 2 , 3)`

giving these parameters: divide_sprite_map($name-for-css, $url-of-image,  $sprite_height, $sprite_width, $number-of-character-columns, $number-of-character-rows, $steps-each-character-takes)



use like this:

```    
let character = "good_guys-"+charIDcol+"-"+charIDrow+"-"+ U/D/L/R +"-"+ walkpos;

            <div class={character} style={charPos}></div>
```
where chirID col and row would be if you have multiple characters in one map, so which column and row they are. In the example png there are 8 characters, each with 12 sprites. To get the second character in the top row, charIDcol=2, charIDrow=1.

<pre>U/D/L/R = up,down,left,right
walkpos = which frame of the animation to use
it is up to you to determine these for your program
</pre>

Thanks to DemonHuntRpg for the example sprite map.
http://demonhuntrpg.deviantart.com/art/Free-Radical-Game-Sprites-Attempt-351569524
