THE FARMER WAS REPLACED
Programming the Farming Drone
 
# Introduction
The Farmer Was Replaced is a game where you program a drone to farm. 
You write simple code to tell the drone what to do, like planting seeds, watering crops, and harvesting. 
As you get better, you can give the drone more complex tasks and make your farm more efficient.

# Table of Contents
-Code Snippets and Explanation (#code-snippets-and-explanation)
-Challenges and Learnings (#challenges-and-learnings)
-References (#references)

#Code-Snippets-and-Explanation
Image and Code

# Step 1: Farming on 1 tile
![](<screenshot/Screenshot 2024-11-02 070156.png>)

**Code:**
```python
harvest()
harvest()
harvest()
harvest()
harvest()
```

**Explanation:**
This is a code for to unlock the while loop as per the game instructions.
And it will only give you 5 hay.

**Notes**
- Using the code above I was able to get 5 hay to unlock the while loops


## Step 2: Farming on 1 tile
**Code:**
```python
while True:
    harvest()
```

**Explanation:**
The code runs an infinite number of times and harvest the grass with the if condition.

**Demo:**
![](<screenshot/Screenshot 2024-11-02 071203.png>)

**Notes**
- Using the code above I was able to get enough hay to unlock the tile
- I was also to unlock speed.

**Challanges**
after unlocking the speed it was difficult to harvest


## Step 3: Farming on 1x3 tile
**Code:**
```python
while True:
    if can_harvest():
        harvest()
```
**Explanation:**
This an code can harvest after unlocking the speed which give increase in hay

**Notes**
I also expand the tile with hay 

**Challanges**
how to move drone to harvest


## Step 4: Farming on 1x3 tile
**Code:**hay              
```python (hay)                        
while True:
    if can_harvest():
        harvest()
    else:
        moce(North)
```
**2code:**bushes
```python (bushes)                        
while True:
    if can_harvest():
        harvest()
        plant(Entities.Bush)
    else:
        moce(North)
```

**Explanation:** 
the above code make sure to harvest the hay and bush while moving on every tile

**Demo:**
![moving drone and harvest](<screenshot/Screenshot 2024-11-02 072656.png>)

**Notes**
- I unlock grass, plant and update the speed of the drone
- have to code differentlly for hay and bush
- unlocked the senses

**Challanges**
making sure that harvest is taking place


## Step 5: Farming on 1x3 tile
**Code:**movement              
```python (movement)                        
if get_pos_y()<=1:
    move(North)
else:
    move(North)
    move(East)
```

**Explanation:** 
the above code will make drone to move on every tiles

**Demo:**
![movement]](<screenshot/Screenshot 2024-11-02 082145.png>)

**Notes**
- I unlock the senses to understand the given number for the every tiles
- I did second expend to grow more and unlock more feature like operator,loops,etc...
- I unlocked carrots to unpdate the speed of the drone
![unlock](<screenshot/Screenshot 2024-11-02 081025.png>)

**Challanges**
- first of all It was hard to understand the senses 
- had to try and figure out a lot of time to make drone move on every tile


## Step 5: Farming on 3x3 tile
**Code:**   carrot           
```python (carrot)                        
while True:
	if can_harvest():
		for i in range(get_world_size()):
			for j in range(get_world_size()):
				move(North)
				harvest()
				till()
				trade(Items.Carrot_Seed)
				plant(Entities.Carrots)
			move(East)
	else:
		move(North)		
```
**Explanation:** 
the above code make sure to till the ground and trade the seed andgrow carrot moving every tile

**Demo:**
![carrots](<screenshot/Screenshot 2024-11-02 175432.png>)

**Notes**
- For loop with get world size make sure to go on every tiles
- I unlocked the function feature with the items that I have 

**Challanges**
- arranging the code and make sure that step are in order like first making ground till and trade and plant   carrot and harvest


## Step 6: Farming on 4x4 tile
After unlocking the function and variable
![after unlocking variables and function](<screenshot/Screenshot 2024-11-03 113140.png>)

**Code:**def with carrot             
```python (def with carrot)                        
	def Boy():
        if num_items(Items.Carrot_Seed)<1:
            trade(Items.Carrot_Seed)
	    else:
            pass
        if can_harvest():
            harvest()
		    till()
		    plant(Entities.Carrots)
	    else:
		    Movement()
```
**Explanation:**
The code controls a farmer who trades for carrot seeds, harvests, tills the land, plants carrots, and moves around. 
I define the function called Boy to trade the seed fisrt and harvest by tilling the soil and planting 
and to be noted that 'Movement()' is also called or change to function

**Demo:**
![called as funtiion](<screenshot/Screenshot 2024-11-02 190323.png>)

**Notes**
- every items/file like hay,bushes and carrot has been now called as funtion because in the main file its not going to be packed
- expend was upgrade to 4x4 
![all code called as funtion](<screenshot/Screenshot 2024-11-03 113104.png>)

**Challanges**
- calling every code as a function and making sure that the function to run in the main file was challanging 


## Step 7: Farming on 4x4 tile
**Code:**tree              
```python (tree)
def Tree():
	x =get_pos_x()
	y =get_pos_y()
	if get_water()<0.76:
		use_item(Items.Water_Tank)
	elif Even(x+y) and can_harvest():
		harvest()
		plant(Entities.Tree)
		Movement()
	else:
		wood()
```
**Explanation:** 
The code defines a function that controls an entity in a game. It checks the water level and the entity's position. If water is low, it uses a water tank. If the position is suitable and harvesting is possible, it harvests, plants a tree, and moves. Otherwise, it gathers wood.

**Demo:**
![alt text](<screenshot/Screenshot 2024-11-03 122506.png>)

**Notes**
- using the above code the number of wood increases faster than from the bushes

**Challanges**
- make tree growable was hard and right amount of water to be pourable on every tiles

After challanges
![alt text](<screenshot/Screenshot 2024-11-03 123236.png>)
![alt text](<screenshot/Screenshot 2024-11-03 123302.png>)


## Step 8: Farming on 5x5 tile
**Code:**Pumpkins             
```python (tree)
def pump():
	if can_harvest():
		for i in range(get_world_size()):
			for j in range(get_world_size()):
				move(North)
				harvest()
				till()
				get_water()
				use_item(Items.Water_Tank)
				trade(Items.Pumpkin_Seed)
				plant(Entities.Pumpkin)
				move(East)
			move(East)
	else:
		move(East)
```
**Explanation:** 
The code implements a strategy for a farming entity in a game. It continuously iterates over the world, harvesting crops, tilling the land, watering crops, trading for pumpkin seeds, planting pumpkins, and moving around. This repetitive action maximizes resource gathering and planting.

**Demo:**
![alt text](<screenshot/Screenshot 2024-11-03 190620.png>)

**Notes**
- using this code i was able to expend the tiles 

**Challanges**
- The code makes a farmer move around the world, harvesting crops, planting seeds, and using water. However, it could be more efficient by reducing unnecessary movement and better managing resources. Additionally, it might struggle in larger worlds or when conditions change.


## Step 9: Farming on 5x5 tile
**Code:**Sunflower             
```python (sunflower)
def sun():
	if can_harvest():
		for i in range(get_world_size()):
			for j in range(get_world_size()):
				move(North)
				harvest()
				till()
				trade(Items.Sunflower_Seed)
				plant(Entities.Sunflower)
				plant(Entities.Tree)
				move(East)
			move(East)
	else:
		move(East)
```
**Explanation:** 
The code defines a function that controls a character in a game. This character focuses on farming sunflowers and trees. It repeatedly moves across the world, harvesting crops, tilling the land, trading for sunflower seeds, and planting both sunflowers and trees. This repetitive pattern aims to maximize resource gathering and planting.

**Demo:**
![alt text](<screenshot/Screenshot 2024-11-03 190201.png>)

**Notes**
- using this code help drone to function faster like flash which mean dron get energy

**Challanges**
-it was challannging for sunflowers to grow as for fist time but i use same code like in pumpkins to funtion code but this code is useful in large tiles

This are the unlock items
![alt text](<screenshot/Screenshot 2024-11-03 191454.png>)
