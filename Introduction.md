# Toribash Scripting SDK Documentation

## Introduction

The Toribash Scripting SDK is full of useful functions and tables of data that should allow one to make most ideas come to life. It provides functionality for tori's, world objects, world state information, player data, camera control, 3D/2D rendering, and plenty more. The goal throughout this documentation is to highlight as close to all functionality as possible, and more importantly, how to use it.

## Table of Contents
- **Introduction**
- **Players**
    - Joint
        - List of joints
        - States
        - Damage
        - Radius
        - Position
    - Part
        - List of parts
        - Position
        - Rotation
        - Velocity
            - Linear/Force
            - Angular/Torque
    - Grip
        - Grip Info
    - Score
    - Bet
    - Information
        - Inventory
            - Items
        - TC/QI/Belt
- **World**
    - Environment Objects
        - Type
            - Dynamic
            - Static
        - Position
        - Size ("sides")
        - Shape
        - Color
        - Model
        - Force
    - Blood
    - Game Rules
    - `get_world_state`
- **User Interface**
    - UIElement
    - Textures
    - Colors (color IDs)
    - `draw_text`
    - `draw_quad`
    - `get_window_size`
    - ...
- **Camera**
    - ...
- **Commands**
    - ...
- **Hooks**
    - `draw2d`
    - `draw3d`
    - `enter_frame`
    - ...
- **Miscellaneous**
    - `open_url`
    - `screenshot`