# Meet the robot!

## Introduction 

You will practice moving and turning the robot to reach the goal.

```customts
    tiles.loadMap(tiles.createMap(tilemap`level1`))
    game.onUpdate(function() {
        if (robot.goalReached(sprites.background.autumn)) {
            game.setGameOverEffect(true, effects.confetti)
            game.setGameOverPlayable(true, music.melodyPlayable(music.powerUp), true)
            game.setGameOverMessage(true, "Goal Reached!")
        }
    })
```

## Step One

Use the ``||robot:begin screen ||`` code to start your robot and place the coins

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
  "main.blocks": "<xml xmlns=\"https://developers.google.com/blockly/xml\"><block type=\"pxt-on-start\" x=\"0\" y=\"0\"></block></xml>",
  "main.ts": "\n",
  "pxt.json": "{\n    \"name\": \"Non Git Hub Robot Tile and Tilemap Assets\",\n    \"description\": \"\",\n    \"dependencies\": {\n        \"device\": \"*\",\n        \"tilemaps\": \"github:microsoft/pxt-tilemaps#v1.12.0\"\n    },\n    \"files\": [\n        \"main.blocks\",\n        \"main.ts\",\n        \"README.md\",\n        \"assets.json\",\n        \"tilemap.g.jres\",\n        \"tilemap.g.ts\"\n    ],\n    \"targetVersions\": {\n        \"branch\": \"v1.13.21\",\n        \"tag\": \"v1.13.21\",\n        \"commits\": \"https://github.com/microsoft/pxt-arcade/commits/5a015bc4703b24f722869cd4356ac2ca288b5800\",\n        \"target\": \"1.13.21\",\n        \"pxt\": \"8.6.47\"\n    },\n    \"preferredEditor\": \"blocksprj\"\n}\n",
  "tilemap.g.jres": "{\n    \"tile1\": {\n        \"data\": \"hwQQABAAAAD//////////09ERERERET0T0RERERERPRPRERERERE9E9ERERERET0T0RERERERPRPRERERERE9E9ERERERET0T0RERERERPRPRERERERE9E9ERERERET0T0RERERERPRPRERERERE9E9ERERERET0T0RERERERPT//////////w==\",\n        \"mimeType\": \"image/x-mkcd-f4\",\n        \"tilemapTile\": true,\n        \"displayName\": \"startTile\"\n    },\n    \"tile2\": {\n        \"data\": \"hwQQABAAAAD//////////4+IiIiIiIj4j4iIiIiIiPiPiIiIiIiI+I+IiIiIiIj4j4iIiIiIiPiPiIiIiIiI+I+IiIiIiIj4j4iIiIiIiPiPiIiIiIiI+I+IiIiIiIj4j4iIiIiIiPiPiIiIiIiI+I+IiIiIiIj4j4iIiIiIiPj//////////w==\",\n        \"mimeType\": \"image/x-mkcd-f4\",\n        \"tilemapTile\": true,\n        \"displayName\": \"goalTile\"\n    },\n    \"tile3\": {\n        \"data\": \"hwQQABAAAAD//////////x8RERERERHxHxEREREREfEfERERERER8R8RERERERHxHxEREREREfEfERERERER8R8RERERERHxHxEREREREfEfERERERER8R8RERERERHxHxEREREREfEfERERERER8R8RERERERHxHxEREREREfH//////////w==\",\n        \"mimeType\": \"image/x-mkcd-f4\",\n        \"tilemapTile\": true,\n        \"displayName\": \"floorTile\"\n    },\n    \"tile4\": {\n        \"data\": \"hwQQABAAAAD//////////393d3d3d3f3f3d3d3d3d/d/d3d3d3d39393d3d3d3f3f3d3d3d3d/d/d3d3d3d39393d3d3d3f3f3d3d3d3d/d/d3d3d3d39393d3d3d3f3f3d3d3d3d/d/d3d3d3d39393d3d3d3f3f3d3d3d3d/f//////////w==\",\n        \"mimeType\": \"image/x-mkcd-f4\",\n        \"tilemapTile\": true,\n        \"displayName\": \"coinTile\"\n    },\n    \"transparency16\": {\n        \"data\": \"hwQQABAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA==\",\n        \"mimeType\": \"image/x-mkcd-f4\",\n        \"tilemapTile\": true\n    },\n    \"level1\": {\n        \"id\": \"level1\",\n        \"mimeType\": \"application/mkcd-tilemap\",\n        \"data\": \"MTAwYTAwMDcwMDA1MDYwNjBkMDYwNjBkMDYwNjA3MGIwMzAzMDMwMzAzMDMwMzAyMDgwYjAzMDMwMzAzMDMwMzAzMDMwODEwMDMwMzAzMDMwMzAzMDMwNDBmMGIwMzAzMDMwMzAzMDMwMzAzMDgwYjAxMDMwNDAzMDQwMzA0MDMwODBhMGMwYzBlMGMwYzBlMGMwYzA5MjIyMjIyMjIyMjAyMDAwMDAwMjAwMjAwMDAwMDIwMDIwMDAwMDAyMDAyMDAwMDAwMjAwMjAwMDAwMDIwMjIyMjIyMjIyMg==\",\n        \"tileset\": [\n            \"myTiles.transparency16\",\n            \"myTiles.tile1\",\n            \"myTiles.tile2\",\n            \"myTiles.tile3\",\n            \"myTiles.tile4\",\n            \"sprites.dungeon.greenOuterNorthWest\",\n            \"sprites.dungeon.greenOuterNorth0\",\n            \"sprites.dungeon.greenOuterNorthEast\",\n            \"sprites.dungeon.greenOuterEast0\",\n            \"sprites.dungeon.greenOuterSouthWest\",\n            \"sprites.dungeon.greenOuterSouthEast\",\n            \"sprites.dungeon.greenOuterWest0\",\n            \"sprites.dungeon.greenOuterSouth1\",\n            \"sprites.dungeon.greenOuterNorth2\",\n            \"sprites.dungeon.greenOuterSouth2\",\n            \"sprites.dungeon.greenOuterEast2\",\n            \"sprites.dungeon.greenOuterWest2\"\n        ],\n        \"displayName\": \"level1\"\n    },\n    \"*\": {\n        \"mimeType\": \"image/x-mkcd-f4\",\n        \"dataEncoding\": \"base64\",\n        \"namespace\": \"myTiles\"\n    }\n}",
  "tilemap.g.ts": "// Auto-generated code. Do not edit.\nnamespace myTiles {\n    //% fixedInstance jres blockIdentity=images._tile\n    export const tile1 = image.ofBuffer(hex``);\n    //% fixedInstance jres blockIdentity=images._tile\n    export const tile2 = image.ofBuffer(hex``);\n    //% fixedInstance jres blockIdentity=images._tile\n    export const tile3 = image.ofBuffer(hex``);\n    //% fixedInstance jres blockIdentity=images._tile\n    export const tile4 = image.ofBuffer(hex``);\n    //% fixedInstance jres blockIdentity=images._tile\n    export const transparency16 = image.ofBuffer(hex``);\n\n    helpers._registerFactory(\"tilemap\", function(name: string) {\n        switch(helpers.stringTrim(name)) {\n            case \"level1\":\n            case \"level1\":return tiles.createTilemap(hex`0a0007000506060d06060d0606070b0303030303030302080b0303030303030303081003030303030303040f0b0303030303030303080b0103040304030403080a0c0c0e0c0c0e0c0c09`, img`\n2 2 2 2 2 2 2 2 2 2 \n2 . . . . . . . . 2 \n2 . . . . . . . . 2 \n2 . . . . . . . . 2 \n2 . . . . . . . . 2 \n2 . . . . . . . . 2 \n2 2 2 2 2 2 2 2 2 2 \n`, [myTiles.transparency16,myTiles.tile1,myTiles.tile2,myTiles.tile3,myTiles.tile4,sprites.dungeon.greenOuterNorthWest,sprites.dungeon.greenOuterNorth0,sprites.dungeon.greenOuterNorthEast,sprites.dungeon.greenOuterEast0,sprites.dungeon.greenOuterSouthWest,sprites.dungeon.greenOuterSouthEast,sprites.dungeon.greenOuterWest0,sprites.dungeon.greenOuterSouth1,sprites.dungeon.greenOuterNorth2,sprites.dungeon.greenOuterSouth2,sprites.dungeon.greenOuterEast2,sprites.dungeon.greenOuterWest2], TileScale.Sixteen);\n        }\n        return null;\n    })\n\n    helpers._registerFactory(\"tile\", function(name: string) {\n        switch(helpers.stringTrim(name)) {\n            case \"startTile\":\n            case \"tile1\":return tile1;\n            case \"goalTile\":\n            case \"tile2\":return tile2;\n            case \"floorTile\":\n            case \"tile3\":return tile3;\n            case \"coinTile\":\n            case \"tile4\":return tile4;\n            case \"transparency16\":return transparency16;\n        }\n        return null;\n    })\n\n}\n// Auto-generated code. Do not edit.\n"
}
```
