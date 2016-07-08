# ShatterLand Client

Free iOS VR game where marble players compete with each other for dominance.


## Game Play

 * Larger players bust smaller players by running into them
 * Players grow by eating fragments scattered on the field
 * Obstacles (large purple spike balls) shoot players into the sky and reduce mass for larger players


## Game Architecture
* Client: Unity3D/C#  ([github.com/mellowDice/ee_client](https://github.com/mellowDice/ee_client))
* Primary Server and Movement Service: Python/Flask ([github.com/mellowDice/ee_server](https://github.com/mellowDice/ee_server))
* Landscape Service: Python/Numpy/Flask ([github.com/mellowDice/landscape-service](https://github.com/mellowDice/landscape-service))
* Field Objects Service: Python/Flask ([github.com/mellowDice/field-objects-service](https://github.com/mellowDice/field-objects-service))
* Data Service: NodeJS/Redis/Express ([github.com/mellowDice/data_service](https://github.com/mellowDice/data_service))
* Web Service: HTML/CSS ([github.com/mellowDice/web_service](https://github.com/mellowDice/web_service))

![Architecture Diagram](https://github.com/mellowDice/ee_diagrams/blob/master/Architecture%20Diagram.jpg?raw=true)


## Client
todo


## Primary Server and Movement Service
todo

## Landscape Service

A fractal mesh-generation implementation using a matrix-based Perlin noise algroithm.

#### Fractal Landscape Generator
The landscape is generated by layering 2D noise of different scales
![Fractal Landscape Diagram](https://github.com/mellowDice/ee_diagrams/blob/master/Fractal%20Noise%20Diagram.jpg?raw=true)
##### Inputs
Octaves: Number of layers to use (maximum may be limited by size of grid); lower octaves are rolling hills; higher octaves are localized bumpiness.

Amplitude Scaling: Each octave's amplitude is scaled by 0.6^(octave no), so lower octaves.

Period Scaling: Each octave's period is (1/1.8)x smaller than the previous octave's period. An octave's period represents the areal width or height of each "bump"


#### Matrix-based 2D Perlin Noise Generator
Generates 2D Noise for input into the fractal landscape generator
![2D Perlin Noise Generator Diagram](https://github.com/mellowDice/ee_diagrams/blob/master/2D%20Noise%20Diagram.jpg?raw=true)


## Field Objects Service
todo

## Web Service
todo
