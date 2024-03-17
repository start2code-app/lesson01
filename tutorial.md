# Rock, paper, scissors 

## @showdialog 
In this project, you'll turn your micro:bit into a Rock, paper, scissors game. 
## 
You don't need ``||basic: on start||`` or ``||basic: forever||`` so drop them back into the toolbox (the middle section). 

```blocks

```
## 
In the Input category, find ``||input: on shake||`` and drag it into the code window. 

```blocks
input.onGesture(Gesture.Shake, function () {
	
})
```

## 
In the Variables category, click on ``||variables: make a variable||`` and call it 'random-number'. 
Find ``||variables: set random_number to 0||`` (in the Variables category) and drop it inside the ``||input: on shake||`` block. 

```blocks
	
input.onGesture(Gesture.Shake, function () {
random_number=0
})
```

## 
To make the game fair, find the ``||math: pick random 0 to 10||`` block (in the Math category). 


Drop it on top of the 0 in ``||variables: set random-number to 0||``. 

```blocks
	
input.onGesture(Gesture.Shake, function () {
random_number =  randint(0, 10)
})
```


## 
In ``||math: pick random 0 to 10||`` change the 0 to 1 and change 1 to 3. 
So now it will pick a random number between 1 and 3, because there are 3 options: rock, paper or scissors. 

```blocks
	
input.onGesture(Gesture.Shake, function () {
random_number =  randint(1, 3)
})
```

## 
Now let's test the 'random-number' variable. Find the ``||logic: if then else||`` block (in the Logic category) and put it under ``||variables: set random-number||``. 


Find the ``||logic: 0 = 0||`` comparison block (in Logic) and drop it on top of 'true'. 

```blocks
input.onGesture(Gesture.Shake, function () {
random_number =  randint(1, 3)
    if 0 == 0
    else
})
```

## 
Find the ``||variables: random-number||`` block (in Variables) and drop it on top of the first 0. 


Then change the second 0 to 1. 

```blocks
input.onGesture(Gesture.Shake, function () {
random_number =  randint(1, 3)
    if random_number  == 1
    else
})
```

## 
Find ``||basic: show icon||`` (in the Basic category) and put it under ``||logic: if||``. 


Change the heart to the small square icon (to represent a rock). 


## 
Use the plus '+' sign to expand the ``||logic: if then else||`` block. 


It will expand the code to have an ``||logic: else if||``.


## 
Similar to before, find ``||logic: 0 = 0||`` (in Logic) and drop it into the gap after ``||logic: else if||``. 
Find the ``||variables: random-number||`` block (in Variables) and drop it on top of the first 0. 


Then change the second 0 to 2. 


## 
Find ``||basic: show icon||`` (in the Basic category) and put it under ``||logic: else if||``. 


Change the heart to the large square icon (to represent paper). 


## 
Let's use logical thinking to make the code more compact. If the random-number variable is between 1 and 3, and it’s not 1 or 2, it must be 3. 


So, add a ``||basic: show icon||`` to show the scissors icon under ``||logic: else||``. 


## 
Test your code out in the simulator by pressing the 'shake' button. 


Do you see the icons for rock, paper and scissors appear randomly? 


## 
Now download your code onto your micro:bit. Press the download button and follow the instructions. 


Try playing Rock, paper, scissors against another micro:bit, or a human! 


## @showdialog 
Congratulations - you have made a micro:bit Rock, paper, scissors game!



