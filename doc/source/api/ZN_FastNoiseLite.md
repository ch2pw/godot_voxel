# ZN_FastNoiseLite

Inherits: [Resource](https://docs.godotengine.org/en/stable/classes/class_resource.html)

Generates coherent and fractal noise using the [FastNoiseLite](https://github.com/Auburn/FastNoiseLite) library.

## Description: 

This is an alternative implementation of [FastNoiseLite](https://docs.godotengine.org/en/stable/classes/class_fastnoiselite.html), based on the same library. Some differences include different default values, and use of period instead of frequency in fractal parameters. It is also used in the voxel module in order to bypass the overhead of Godot calls in GDExtension builds.

## Properties: 


Type                                                                      | Name                                                         | Default                            
------------------------------------------------------------------------- | ------------------------------------------------------------ | -----------------------------------
[CellularDistanceFunction](ZN_FastNoiseLite.md#enumerations)              | [cellular_distance_function](#i_cellular_distance_function)  | CELLULAR_DISTANCE_EUCLIDEAN_SQ (1) 
[float](https://docs.godotengine.org/en/stable/classes/class_float.html)  | [cellular_jitter](#i_cellular_jitter)                        | 1.0                                
[CellularReturnType](ZN_FastNoiseLite.md#enumerations)                    | [cellular_return_type](#i_cellular_return_type)              | CELLULAR_RETURN_DISTANCE (1)       
[float](https://docs.godotengine.org/en/stable/classes/class_float.html)  | [fractal_gain](#i_fractal_gain)                              | 0.5                                
[float](https://docs.godotengine.org/en/stable/classes/class_float.html)  | [fractal_lacunarity](#i_fractal_lacunarity)                  | 2.0                                
[int](https://docs.godotengine.org/en/stable/classes/class_int.html)      | [fractal_octaves](#i_fractal_octaves)                        | 3                                  
[float](https://docs.godotengine.org/en/stable/classes/class_float.html)  | [fractal_ping_pong_strength](#i_fractal_ping_pong_strength)  | 2.0                                
[FractalType](ZN_FastNoiseLite.md#enumerations)                           | [fractal_type](#i_fractal_type)                              | FRACTAL_FBM (1)                    
[float](https://docs.godotengine.org/en/stable/classes/class_float.html)  | [fractal_weighted_strength](#i_fractal_weighted_strength)    | 0.0                                
[NoiseType](ZN_FastNoiseLite.md#enumerations)                             | [noise_type](#i_noise_type)                                  | TYPE_OPEN_SIMPLEX_2 (0)            
[float](https://docs.godotengine.org/en/stable/classes/class_float.html)  | [period](#i_period)                                          | 64.0                               
[RotationType3D](ZN_FastNoiseLite.md#enumerations)                        | [rotation_type_3d](#i_rotation_type_3d)                      | ROTATION_3D_NONE (0)               
[int](https://docs.godotengine.org/en/stable/classes/class_int.html)      | [seed](#i_seed)                                              | 0                                  
[ZN_FastNoiseLiteGradient](ZN_FastNoiseLiteGradient.md)                   | [warp_noise](#i_warp_noise)                                  |                                    
<p></p>

## Methods: 


Return                                                                    | Signature                                                                                                                                                                                                                                                               
------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
[float](https://docs.godotengine.org/en/stable/classes/class_float.html)  | [get_noise_2d](#i_get_noise_2d) ( [float](https://docs.godotengine.org/en/stable/classes/class_float.html) x, [float](https://docs.godotengine.org/en/stable/classes/class_float.html) y )                                                                              
[float](https://docs.godotengine.org/en/stable/classes/class_float.html)  | [get_noise_2dv](#i_get_noise_2dv) ( [Vector2](https://docs.godotengine.org/en/stable/classes/class_vector2.html) position )                                                                                                                                             
[float](https://docs.godotengine.org/en/stable/classes/class_float.html)  | [get_noise_3d](#i_get_noise_3d) ( [float](https://docs.godotengine.org/en/stable/classes/class_float.html) x, [float](https://docs.godotengine.org/en/stable/classes/class_float.html) y, [float](https://docs.godotengine.org/en/stable/classes/class_float.html) z )  
[float](https://docs.godotengine.org/en/stable/classes/class_float.html)  | [get_noise_3dv](#i_get_noise_3dv) ( [Vector3](https://docs.godotengine.org/en/stable/classes/class_vector3.html) position )                                                                                                                                             
<p></p>

## Enumerations: 

enum **NoiseType**: 

- <span id="i_TYPE_OPEN_SIMPLEX_2"></span>**TYPE_OPEN_SIMPLEX_2** = **0**
- <span id="i_TYPE_OPEN_SIMPLEX_2S"></span>**TYPE_OPEN_SIMPLEX_2S** = **1**
- <span id="i_TYPE_CELLULAR"></span>**TYPE_CELLULAR** = **2**
- <span id="i_TYPE_PERLIN"></span>**TYPE_PERLIN** = **3**
- <span id="i_TYPE_VALUE_CUBIC"></span>**TYPE_VALUE_CUBIC** = **4**
- <span id="i_TYPE_VALUE"></span>**TYPE_VALUE** = **5**

enum **FractalType**: 

- <span id="i_FRACTAL_NONE"></span>**FRACTAL_NONE** = **0**
- <span id="i_FRACTAL_FBM"></span>**FRACTAL_FBM** = **1**
- <span id="i_FRACTAL_RIDGED"></span>**FRACTAL_RIDGED** = **2**
- <span id="i_FRACTAL_PING_PONG"></span>**FRACTAL_PING_PONG** = **3**

enum **RotationType3D**: 

- <span id="i_ROTATION_3D_NONE"></span>**ROTATION_3D_NONE** = **0**
- <span id="i_ROTATION_3D_IMPROVE_XY_PLANES"></span>**ROTATION_3D_IMPROVE_XY_PLANES** = **1**
- <span id="i_ROTATION_3D_IMPROVE_XZ_PLANES"></span>**ROTATION_3D_IMPROVE_XZ_PLANES** = **2**

enum **CellularDistanceFunction**: 

- <span id="i_CELLULAR_DISTANCE_EUCLIDEAN"></span>**CELLULAR_DISTANCE_EUCLIDEAN** = **0**
- <span id="i_CELLULAR_DISTANCE_EUCLIDEAN_SQ"></span>**CELLULAR_DISTANCE_EUCLIDEAN_SQ** = **1**
- <span id="i_CELLULAR_DISTANCE_MANHATTAN"></span>**CELLULAR_DISTANCE_MANHATTAN** = **2**
- <span id="i_CELLULAR_DISTANCE_HYBRID"></span>**CELLULAR_DISTANCE_HYBRID** = **3**

enum **CellularReturnType**: 

- <span id="i_CELLULAR_RETURN_CELL_VALUE"></span>**CELLULAR_RETURN_CELL_VALUE** = **0**
- <span id="i_CELLULAR_RETURN_DISTANCE"></span>**CELLULAR_RETURN_DISTANCE** = **1**
- <span id="i_CELLULAR_RETURN_DISTANCE_2"></span>**CELLULAR_RETURN_DISTANCE_2** = **2**
- <span id="i_CELLULAR_RETURN_DISTANCE_2_ADD"></span>**CELLULAR_RETURN_DISTANCE_2_ADD** = **3**
- <span id="i_CELLULAR_RETURN_DISTANCE_2_SUB"></span>**CELLULAR_RETURN_DISTANCE_2_SUB** = **4**
- <span id="i_CELLULAR_RETURN_DISTANCE_2_MUL"></span>**CELLULAR_RETURN_DISTANCE_2_MUL** = **5**
- <span id="i_CELLULAR_RETURN_DISTANCE_2_DIV"></span>**CELLULAR_RETURN_DISTANCE_2_DIV** = **6**


## Property Descriptions

### [CellularDistanceFunction](ZN_FastNoiseLite.md#enumerations)<span id="i_cellular_distance_function"></span> **cellular_distance_function** = CELLULAR_DISTANCE_EUCLIDEAN_SQ (1)

*(This property has no documentation)*

### [float](https://docs.godotengine.org/en/stable/classes/class_float.html)<span id="i_cellular_jitter"></span> **cellular_jitter** = 1.0

*(This property has no documentation)*

### [CellularReturnType](ZN_FastNoiseLite.md#enumerations)<span id="i_cellular_return_type"></span> **cellular_return_type** = CELLULAR_RETURN_DISTANCE (1)

*(This property has no documentation)*

### [float](https://docs.godotengine.org/en/stable/classes/class_float.html)<span id="i_fractal_gain"></span> **fractal_gain** = 0.5

*(This property has no documentation)*

### [float](https://docs.godotengine.org/en/stable/classes/class_float.html)<span id="i_fractal_lacunarity"></span> **fractal_lacunarity** = 2.0

*(This property has no documentation)*

### [int](https://docs.godotengine.org/en/stable/classes/class_int.html)<span id="i_fractal_octaves"></span> **fractal_octaves** = 3

*(This property has no documentation)*

### [float](https://docs.godotengine.org/en/stable/classes/class_float.html)<span id="i_fractal_ping_pong_strength"></span> **fractal_ping_pong_strength** = 2.0

*(This property has no documentation)*

### [FractalType](ZN_FastNoiseLite.md#enumerations)<span id="i_fractal_type"></span> **fractal_type** = FRACTAL_FBM (1)

*(This property has no documentation)*

### [float](https://docs.godotengine.org/en/stable/classes/class_float.html)<span id="i_fractal_weighted_strength"></span> **fractal_weighted_strength** = 0.0

*(This property has no documentation)*

### [NoiseType](ZN_FastNoiseLite.md#enumerations)<span id="i_noise_type"></span> **noise_type** = TYPE_OPEN_SIMPLEX_2 (0)

*(This property has no documentation)*

### [float](https://docs.godotengine.org/en/stable/classes/class_float.html)<span id="i_period"></span> **period** = 64.0

*(This property has no documentation)*

### [RotationType3D](ZN_FastNoiseLite.md#enumerations)<span id="i_rotation_type_3d"></span> **rotation_type_3d** = ROTATION_3D_NONE (0)

*(This property has no documentation)*

### [int](https://docs.godotengine.org/en/stable/classes/class_int.html)<span id="i_seed"></span> **seed** = 0

*(This property has no documentation)*

### [ZN_FastNoiseLiteGradient](ZN_FastNoiseLiteGradient.md)<span id="i_warp_noise"></span> **warp_noise**

*(This property has no documentation)*

## Method Descriptions

### [float](https://docs.godotengine.org/en/stable/classes/class_float.html)<span id="i_get_noise_2d"></span> **get_noise_2d**( [float](https://docs.godotengine.org/en/stable/classes/class_float.html) x, [float](https://docs.godotengine.org/en/stable/classes/class_float.html) y ) 

*(This method has no documentation)*

### [float](https://docs.godotengine.org/en/stable/classes/class_float.html)<span id="i_get_noise_2dv"></span> **get_noise_2dv**( [Vector2](https://docs.godotengine.org/en/stable/classes/class_vector2.html) position ) 

*(This method has no documentation)*

### [float](https://docs.godotengine.org/en/stable/classes/class_float.html)<span id="i_get_noise_3d"></span> **get_noise_3d**( [float](https://docs.godotengine.org/en/stable/classes/class_float.html) x, [float](https://docs.godotengine.org/en/stable/classes/class_float.html) y, [float](https://docs.godotengine.org/en/stable/classes/class_float.html) z ) 

*(This method has no documentation)*

### [float](https://docs.godotengine.org/en/stable/classes/class_float.html)<span id="i_get_noise_3dv"></span> **get_noise_3dv**( [Vector3](https://docs.godotengine.org/en/stable/classes/class_vector3.html) position ) 

*(This method has no documentation)*

_Generated on May 15, 2025_
