In this project, we develop a <strong>cellular automaton</strong>, to model the <strong>propagation of a forest fire</strong>. A cellular automaton is a grid of cells (with $n$ rows and $m$ columns), each in a particular state at each time $t$. The state of a cell at time $t + 1$ depends on :<br/>
- The state of neighboring cells on the grid.<br/>
- Its state at the previous time $(t)$ based on transition rules.<br/>

Here, the transition rules represent the rules of fire propagation, defined as follows :<br/>
1. At the initial state $t$, the forest has a certain <strong>density</strong> : each cell contains either a healthy tree with a probability $p$, or bare ground with a probability $1 - p$.<br/>
2. We randomly set fire on one of the trees.<br/>
3. The fire propagates : an empty cell remains empty, a healthy tree that is a (Van Neumann) neighbor to a burning tree catches fire, a healthy tree with no burning neighbors remains healthy, a burning tree becomes a burned tree, a burned tree remains burned.

We model this phenomenon using an <strong>object-oriented approach</strong> in Python. Our goal is to refine the model as we progress and derive a purpose : visualize how the fire behaves over time (the number of program iterations) by parameterizing different conditions such as forest density, weather, or firefighters intervention.

Initially, our forest is a simple matrix, then it has a <strong>torus-shaped topology</strong>, allowing us to better represent the reality of a forest by avoiding edge effects. Finally, our work will feature a <strong>graphical interface</strong> for a dynamic and visual representation, using the Python tkinter library.</br> 
NB: This work is accompanied by a <strong>UML diagram</strong> depicting the architecture of our model (all classes, their attributes, and methods).</br>
NB2: All attributes are protected within the class (encapsulated), but some are accessible through setter and getter methods. The methods are considered public when they can be called by the user ; otherwise, they are encapsulated.
