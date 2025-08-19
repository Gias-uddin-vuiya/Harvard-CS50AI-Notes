## Search


### Search Problems

- Inital state (some place where we gegin)

- actions (some sort of action that we can take or multiple action that we can take in any given state)

- transition model (some way of defining what happens when we go from one state and make one action what state do we end up with as a result)

- goal test (In additon to that, we need some goal test to know whether or not we've reached a goal)

- path cost funciton (path cost function that tells us for any particular path by following some sequence of actions, how expensive is that path.)


The goal, ultimately, is to find a soluiton, where a solution in this case is just some sequence of actions that will take us from the initial state to a goal state.


## Node
a data structure that keeps track of 
- a state

- a parent (node that generated this node)

- an action (action applied to parent to get node)

- a path cost (from initial state to node)

So this is the data structure that we've going to use in order to solve the problem.

`ENG: Now let's talk about the approach, how might we actually begin to solve the problem?`

`ENG: Well, as you might imagine, what we've going to do is we're going to start at one particular state and we're just going to explore from there.`

### Approach

- Start with a frontier that contains the initial state.

- Repeat: 
    - If the frontier is empty, then no solution
    - Remove a node from the frontier
    - If node contains goal state. return the solution.
    - Expand node, add resulting nodes to the frontier.

And then we'll repeat the process.


`Note: I'll explore the example problem`

`ENG: So this is the general idea, the gner4eal approach of thi search alogorithm`

`ENG: So the next question you might reasonably ask is, what could go wrong here?`

`What are the potential problmes with an approach like this?`


### Revised Approach

Better way to solve search problem. And it's going to look veyr similar just with a couple of modifications.


**Note: Frontier is a data structure**

## Stack
last-in first-out data type.

Which means the last thing that I add to the frontier
is going to be the first thing that I remove from the frontier.

## Depth-First Search

Depth first search is the search algorithm where we always explore the deepest node in the frontier.
We keep going deeper and deeper through our search tree. And then if we hit a dead end, we back up and we try soemthing else instead.


## Breadth-First Search

Which behaves very similarly to depth-first search with one differnece. Instead of always exploring the deepest node in the search tree the way the depth first search does. 

Breath-first search algorithm that always expands the shallowest node in the frontier.

`ENG: What is that means?`

`ENG: Well, it means that instead of using a stack, which DFS, used where the most recent item added to the frontier is the one we'll explore next, in breath firs search, or BFS, will instead use a queue where a queue is a first in, first out data structure`

## queue

first-in first-out data type.


Where the very first thing we add to the frontier is the first one
we'll explore. And they effectively form a line or a queue, where the earlier you arrive in the frontier, the earlier you get explored.

`ENG: One thing you might reasonably ask is, is this algorithm always going to work?`


`ENG: Is it going to be a good solution?`

`ENG: And the answer there is not necessarily.`


