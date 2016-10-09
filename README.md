use this scss to make classes for each of your sprites from a sprite map.

in your main.scss   `@import "{}/imports/ui/scss/sprites";`

and then create your classes with something like:
`@include divide_sprite_map('good_guys', 'sprites_by_demonhuntrpg_transparent.png', 32px, 32px, 4 , 2 , 3)`

giving these parameters: divide_sprite_map($name-for-css, $url-of-image,  $sprite_height, $sprite_width, $number-of-character-columns, $number-of-character-rows, $steps-each-character-takes)



use like this:

```    
let character = "good_guys-"+charIDcol+"-"+charIDrow+"-"+ U/D/L/R +"-"+ this.state.walkpos;

            <div class={character} style={charPos}></div>
```


Thanks to DemonHuntRpg for the example sprite map.
http://demonhuntrpg.deviantart.com/art/Free-Radical-Game-Sprites-Attempt-351569524
