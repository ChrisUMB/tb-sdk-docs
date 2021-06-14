# Joint

## Overview

A joint is one of the 20 spherical connections between body parts. They each can have their own state, and by changing the states of the joints on a tori, you play the game. Joints can be dismembered, meaning the connection they represent between two body parts is broken, and the parts can separate freely of one another. A joint can also fracture, meaning that the player cannot control it's state, and it will rotate about it's axis much more freely than normally.

## Table of Contents

- States
- Damage
- Radius
- Position

## List of Joints
This is a list of the joints. It is mapped as numerical index, name, and inversion. Don't worry about what inversion means quite yet, it's explained later.
```
0       neck            false
1       chest           false
2       lumbar          false
3       abs             true
4       r_pec           false
5       r_shoulder      false
6       r_elbow         false
7       l_pec           false
8       l_shoulder      false
9       l_elbow         false
10      r_wrist         false
11      l_wrist         false
12      r_glute         true
13      l_glute         true
14      r_hip           true
15      l_hip           true
16      r_knee          false
17      l_knee          false
18      r_ankle         true
19      l_ankle         true
```

## States

Joint states, at first, sound simple; you can extend, contract, relax, and hold joints. Some of these states have synonyms depending on the joint you are changing the state of, such as the chest having a rotate and the lumbar having a bend, but they are still the same four states internally.

## List of States

This is a list of the joint states. It is mapped as numerical index, name, and list of alternative names if present. 

**States are not consistent for each joint, see inversions.**
```
1       extend      (lower, right rotate, right bend)
2       contract    (raise, left rotate, left bend)
3       hold
4       relax
```

## Inversion

Some joints are inverted, meaning that appying state `1`, which would extend if applied to the neck, would actually contract if applied to the abs. This has to do with the natural order that the game works in when toggling through joint states. You'll notice that if you pick any joint in the joints list that is not inverted, and you click through the states in game starting at `relax`, it will go in the right order. But when you take a joint that is inverted, it will go `contract`, `extend`. Scrolling up/down on joints showcases this idea a bit better.

## Code

To get the state of a joint, you would use:

- `get_joint_info(player_index, joint_index).state`.

 To set the state of a joint, you would use:

- `set_joint_state(player_index, joint_index, state_index)`

`get_joint_info` returns a table of information you can access that looks like:

```
    state = <index of the state>
    screen_state = <name of the state>
    name = <name of the joint>
    mod_name = <name of the joint used in modmaker>
```

