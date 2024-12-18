# Pathfinding
 
A simple djikstra pathfinding algorithm used in luau. 

## Introduction
This library defines position points as PointData, which in detail is as follows:

```
PointData = {
	PointId : number,            --the id of the point 
	["Neighbours"] : { 
		[number] : PointData 
	},                           -- the point's neighbour(s)
	Obstacled : boolean,         -- if the point cannot be passed
	Cost : number,               -- the higher the cost, the less likely the algorithm chooses this point to pass through

	Came_From : PointData ?      -- used internally - not needed to be used
}
```
## Installation
### Wally 
pathfinding = "krungkualalumpur/pathfinding@0.1.1"

## How to use?
Use the method ```djikstraPathfinding``` for performance optimized pathfinding search.

Start by passing neccessary parameters 
```
pathfinding.djikstraPathfinding(
    PointsData,     -- a table consisting PointData
    startPoint,     -- the starting point in the form of PointData
    endPoint        -- the ending point in the form of Point Data
)
```
