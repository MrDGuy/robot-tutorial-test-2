# Create a Character

## Introduction 

Explore with the robot!

## Step One

Create a Tile map using the ``||tiles:tilemap||`` code to create a map.  Clock on the map icon.

```python
level1 = tiles.create_map(tilemap("""level1"""))
```

## Step Two

Use the ``||tiles:set current tilemap to ||`` code to reveal the tilemap to the screen

```python
tiles.load_map(level1)
```

## Step Three

Use the ``||robot:begin screen ||`` code to start your robot and place the coins

```python
robot.begin_screen()
```

## Step Four

Use the ``||robot:move forward||`` block to move the robot.

```python
robot.move_forward()
```

## Step Five

Determine whether the robot can move using the ``||robot:can move||`` block.

```python
if robot.can_move("right"):
    robot.turn_right()
elif robot.can_move("left"):
    robot.turn_left()

```

## Step Six

Collect any coins with the detect coin ``||robot:detect coin||`` block.

```python
if robot.detect_coin():
    robot.collect_coin()
```
