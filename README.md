<h1>ExpNo 5 : Implement Simple Hill Climbing Algorithm</h1> 
<h3>Name:HARISH GOWTHAM E         </h3>
<h3>Register Number: 2305002009          </h3>
<H3>Aim:</H3>
<p>Implement Simple Hill Climbing Algorithm and Generate a String by Mutating a Single Character at each iteration </p>
<h2> Theory: </h2>
<p>Hill climbing is a variant of Generate and test in which feedback from test procedure is used to help the generator decide which direction to move in search space.
Feedback is provided in terms of heuristic function
</p>


<h2>Algorithm:</h2>


1.Choose a starting point (initial solution).

2.Calculate its value using the objective function f(x).

3.Generate a neighbor (small change, e.g., move left or right).

4.Compare values:

    If the neighbor is better, move to it.

    Otherwise, stay at the current point.

5.Repeat steps 3–4 until the maximum number of iterations is reached, then return the best solution.

## PROGRAM
```python
import random

# Objective function (we want to maximize this)
def f(x):
    return -(x - 3)**2 + 9  # Peak at x = 3

def hill_climb(start, max_iterations, step_size):
    current = start
    for i in range(max_iterations):
        # Generate a neighbor (move left or right by step_size)
        neighbor = current + random.choice([-step_size, step_size])
        
        # If neighbor is better, move there
        if f(neighbor) > f(current):
            current = neighbor
    
    return current, f(current)

# Run hill climbing
best_x, best_value = hill_climb(start=random.uniform(-10, 10), 
                                max_iterations=1000, 
                                step_size=0.1)

print("Best solution x:", best_x)
print("Best value f(x):", best_value)
```
   
## Input 

Start = -6.52
max_iterations = 1000
step_size = 0.1


## Output
<img width="427" height="57" alt="image" src="https://github.com/user-attachments/assets/d0772de0-e67a-41aa-8a38-3214a38daf24" />


## Result
Thus the given program for Hill Climbing Algorithm was implemented and executed successfully

