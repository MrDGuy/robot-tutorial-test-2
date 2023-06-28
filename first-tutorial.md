# Meet the robot!

## Introduction 

You will practice moving and turning the robot to reach the goal.

```customts
    tiles.loadMap(tiles.createMap(tilemap`level1`))
    robot.beginScreen()
    game.onUpdate(function () {
        if (robot.goalReached()) {
            music.play(music.melodyPlayable(music.powerUp), music.PlaybackMode.UntilDone)
            game.splash("You reached the goal!")
            game.reset()
        }
    })
```

## Step One

Use the ``||robot:begin screen ||`` code to start your robot on the start tile and set up the tilemap.

```python
robot.begin_screen()
```

## Step Two

Use the ``||robot:move forward||`` block to move the robot.

```python
robot.move_forward()
```

## Step Three

Change the direction the robot is facing with the ``||robot:turn right||`` and ``||robot:turn left||`` blocks.

```python
robot.turn_right()
robot.turn_left()

```

## Step Four

Move the robot to the goal square (blue square) to complete the program.


```assetjson
{
  "README.md": " ",
  "assets.json": "",
  "main.blocks": "<xml xmlns=\"https://developers.google.com/blockly/xml\"><block type=\"pxt-on-start\" x=\"0\" y=\"0\"><statement name=\"HANDLER\"><block type=\"tilemap_loadMap\"><value name=\"map\"><shadow type=\"create_overworld_map\"><field name=\"tilemap\">tilemap`level1`</field><data>{\"commentRefs\":[],\"fieldData\":{\"tilemap\":\"level1\"}}</data></shadow></value><next><block type=\"robot_beginScreen\"></block></next></block></statement></block><block type=\"gameupdate\" x=\"390\" y=\"90\"><statement name=\"HANDLER\"><block type=\"controls_if\"><value name=\"IF0\"><shadow type=\"logic_boolean\"><field name=\"BOOL\">TRUE</field></shadow><block type=\"robot_goalReached\"></block></value><statement name=\"DO0\"><block type=\"music_playable_play\"><field name=\"playbackMode\">music.PlaybackMode.UntilDone</field><value name=\"toPlay\"><shadow type=\"music_melody_playable\"><field name=\"melody\">music.baDing</field></shadow><block type=\"music_melody_playable\"><field name=\"melody\">music.powerUp</field></block></value><next><block type=\"gameSplash\"><mutation xmlns=\"http://www.w3.org/1999/xhtml\" _expanded=\"0\" _input_init=\"true\"></mutation><value name=\"title\"><shadow type=\"text\"><field name=\"TEXT\">You reached the goal!</field></shadow></value><value name=\"subtitle\"><shadow type=\"text\"><field name=\"TEXT\"></field></shadow></value><next><block type=\"arcade_game_reset\"></block></next></block></next></block></statement></block></statement></block></xml>",
  "main.ts": "tiles.loadMap(tiles.createMap(tilemap`level1`))\nrobot.beginScreen()\ngame.onUpdate(function () {\n    if (robot.goalReached()) {\n        music.play(music.melodyPlayable(music.powerUp), music.PlaybackMode.UntilDone)\n        game.splash(\"You reached the goal!\")\n        game.reset()\n    }\n})\n",
  "pxt.json": "{\n    \"name\": \"Basic Template for Code and Asset Creation\",\n    \"description\": \"\",\n    \"dependencies\": {\n        \"device\": \"*\",\n        \"tilemaps\": \"github:microsoft/pxt-tilemaps#v1.12.0\",\n        \"Sprite Grid\": \"github:microsoft/arcade-grid#v1.3.0\",\n        \"Robot Extension\": \"github:MrDGuy/robot-extension#45f0768a5e0c25e4123c6e65e56115a7d468331b\"\n    },\n    \"files\": [\n        \"main.blocks\",\n        \"main.ts\",\n        \"README.md\",\n        \"assets.json\",\n        \"tilemap.g.jres\",\n        \"tilemap.g.ts\"\n    ],\n    \"targetVersions\": {\n        \"branch\": \"v1.13.26\",\n        \"tag\": \"v1.13.26\",\n        \"commits\": \"https://github.com/microsoft/pxt-arcade/commits/55a70d58dd8d2cfb8363bc6fa31de4c829c33a4d\",\n        \"target\": \"1.13.26\",\n        \"pxt\": \"9.1.3\"\n    },\n    \"preferredEditor\": \"tsprj\"\n}\n",
  "tilemap.g.jres": "{\n    \"tile1\": {\n        \"data\": \"hwQQABAAAAD//////////09ERERERET0T0RERERERPRPRERERERE9E9ERERERET0T0RERERERPRPRERERERE9E9ERERERET0T0RERERERPRPRERERERE9E9ERERERET0T0RERERERPRPRERERERE9E9ERERERET0T0RERERERPT//////////w==\",\n        \"mimeType\": \"image/x-mkcd-f4\",\n        \"tilemapTile\": true,\n        \"displayName\": \"startTile\"\n    },\n    \"tile2\": {\n        \"data\": \"hwQQABAAAAD//////////x8RERERERHxHxEREREREfEfERERERER8R8RERERERHxHxEREREREfEfERERERER8R8RERERERHxHxEREREREfEfERERERER8R8RERERERHxHxEREREREfEfERERERER8R8RERERERHxHxEREREREfH//////////w==\",\n        \"mimeType\": \"image/x-mkcd-f4\",\n        \"tilemapTile\": true,\n        \"displayName\": \"floorTile\"\n    },\n    \"tile3\": {\n        \"data\": \"hwQQABAAAAD//////////4+IiIiIiIj4j4iIiIiIiPiPiIiIiIiI+I+IiIiIiIj4j4iIiIiIiPiPiIiIiIiI+I+IiIiIiIj4j4iIiIiIiPiPiIiIiIiI+I+IiIiIiIj4j4iIiIiIiPiPiIiIiIiI+I+IiIiIiIj4j4iIiIiIiPj//////////w==\",\n        \"mimeType\": \"image/x-mkcd-f4\",\n        \"tilemapTile\": true,\n        \"displayName\": \"goalTile\"\n    },\n    \"tile4\": {\n        \"data\": \"hwQQABAAAAD//////////393d3d3d3f3f3d3d3d3d/d/d3d3d3d39393d3d3d3f3f3d3d3d3d/d/d3d3d3d39393d3d3d3f3f3d3d3d3d/d/d3d3d3d39393d3d3d3f3f3d3d3d3d/d/d3d3d3d39393d3d3d3f3f3d3d3d3d/f//////////w==\",\n        \"mimeType\": \"image/x-mkcd-f4\",\n        \"tilemapTile\": true,\n        \"displayName\": \"coinTile\"\n    },\n    \"transparency16\": {\n        \"data\": \"hwQQABAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA==\",\n        \"mimeType\": \"image/x-mkcd-f4\",\n        \"tilemapTile\": true\n    },\n    \"level1\": {\n        \"id\": \"level1\",\n        \"mimeType\": \"application/mkcd-tilemap\",\n        \"data\": \"MTAwYTAwMDcwMDA0MDQwNDA0MDQwNDA0MDQwNDA0MDQwMjAyMDIwMjAyMDIwMjAzMDQwNDAyMDIwMjAyMDIwMjAyMDIwNDA0MDIwMjAyMDIwMjAyMDIwMjA0MDQwMjAyMDIwMjAyMDIwMjAyMDQwNDAxMDIwMjAyMDIwMjAyMDIwNDA0MDQwNDA0MDQwNDA0MDQwNDA0MDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMA==\",\n        \"tileset\": [\n            \"myTiles.transparency16\",\n            \"myTiles.tile1\",\n            \"myTiles.tile2\",\n            \"myTiles.tile3\",\n            \"sprites.builtin.forestTiles0\"\n        ],\n        \"displayName\": \"level1\"\n    },\n    \"*\": {\n        \"mimeType\": \"image/x-mkcd-f4\",\n        \"dataEncoding\": \"base64\",\n        \"namespace\": \"myTiles\"\n    }\n}",
  "tilemap.g.ts": "// Auto-generated code. Do not edit.\nnamespace myTiles {\n    //% fixedInstance jres blockIdentity=images._tile\n    export const tile1 = image.ofBuffer(hex``);\n    //% fixedInstance jres blockIdentity=images._tile\n    export const tile2 = image.ofBuffer(hex``);\n    //% fixedInstance jres blockIdentity=images._tile\n    export const tile3 = image.ofBuffer(hex``);\n    //% fixedInstance jres blockIdentity=images._tile\n    export const tile4 = image.ofBuffer(hex``);\n    //% fixedInstance jres blockIdentity=images._tile\n    export const transparency16 = image.ofBuffer(hex``);\n\n    helpers._registerFactory(\"tilemap\", function(name: string) {\n        switch(helpers.stringTrim(name)) {\n            case \"level1\":\n            case \"level1\":return tiles.createTilemap(hex`0a00070004040404040404040404040202020202020203040402020202020202020404020202020202020204040202020202020202040401020202020202020404040404040404040404`, img`\n. . . . . . . . . . \n. . . . . . . . . . \n. . . . . . . . . . \n. . . . . . . . . . \n. . . . . . . . . . \n. . . . . . . . . . \n. . . . . . . . . . \n`, [myTiles.transparency16,myTiles.tile1,myTiles.tile2,myTiles.tile3,sprites.builtin.forestTiles0], TileScale.Sixteen);\n        }\n        return null;\n    })\n\n    helpers._registerFactory(\"tile\", function(name: string) {\n        switch(helpers.stringTrim(name)) {\n            case \"startTile\":\n            case \"tile1\":return tile1;\n            case \"floorTile\":\n            case \"tile2\":return tile2;\n            case \"goalTile\":\n            case \"tile3\":return tile3;\n            case \"coinTile\":\n            case \"tile4\":return tile4;\n            case \"transparency16\":return transparency16;\n        }\n        return null;\n    })\n\n}\n// Auto-generated code. Do not edit.\n"
}
```
