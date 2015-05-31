# jQuery Brackets
Plugin jQuery for create tournament brackets

### Simple usage:

```javascript
rounds = [
    [

        {
            player1: {
                name: "Player 1",               //-- name of the player
                winner: true,                   //-- add class winner to player container
                ID: 1,                          //-- player ID
                url: "http://custom_link.com"   //-- action click to player
            },
            player2: {
                name: "Player 2",
                ID: 2
            },
        },
    ],

    [

        {
            player1: { name: "Player 1", winner: true, ID: 1, url: "http://custom_link.com" },
        },
    ]
];

$('selector').brackets({
    rounds: rounds //-- JSON with matches of the each round
});

------------------------------------------
Result
------------------------------------------

 -----------
|  Player 1 |-------,
 -----------    -----------
               |  Player 1 |
 -----------    -----------
|  Player 2 |-------'
 -----------

```


### Advance usage:

```javascript
var titles = ['Ronda 1', 'Ronda 2', 'Ronda 3', 'Ronda 4', 'Ronda 5']; //-- example titles

//-- All colors can be hexadecimal or string name

$(".brackets").brackets({
            titles: titles,                 //-- (Array) with titles for each round -- default: false -- if the value is true, then add titles automatically
            rounds: rounds,                 //-- (Required) Array with matches ( JSON ) for each round
            color_title: 'black',           //-- (String) Color of the title text
            border_color: '#00F',           //-- (String) Border color of the line of brackets
            color_player: 'black',          //-- (String) Color of the player text (name)
            bg_player: 'white',             //-- (String) Background color of the player container
            color_player_hover: 'white',    //-- (String) Color of the player text (name) when mouse is hover
            bg_player_hover: 'blue',        //-- (String) Background color of the player container when mouse is hover
            border_radius_player: '10px',   //-- (String) Border radius of the player container
            border_radius_lines: '10px',    //-- (String) Border radius of the lines that join rounds
        });

```


### Default values:

```javascript

$(".brackets").brackets({
    titles: false,          //-- If the value is true, then add titles automatically
    color_title: 'black',
    border_color: 'black',
    color_player: 'black',
    bg_player: 'white',
    color_player_hover: 'black',
    bg_player_hover: 'white',
    border_radius_player: '0px',
    border_radius_lines: '0px'
});

```

## Author

* [Ali Camargo](http://github.com/alicamargom)