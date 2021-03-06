# Smoov & Curly's Bogus Journey

## Decision making & Reinforcement Learning
- Supervised learning
- Unsupervised learning 
- Reinforcement learning: give x and z, learn some function that can generate y.
- ![learnings_p1](https://raw.githubusercontent.com/suereey/RL_CS7642_Fall2021_StudyNotes/main/screenshot/P1_01.PNG)

## The world Example
- Steps to achieve goal
	- ![p2](https://raw.githubusercontent.com/suereey/RL_CS7642_Fall2021_StudyNotes/main/screenshot/P1_02.PNG)
- What if uncertainty invovles?
	- ![p3](https://raw.githubusercontent.com/suereey/RL_CS7642_Fall2021_StudyNotes/main/screenshot/P1_03.PNG)
- Markov Decision Processes
	- Markov property is only th epresent matters || Things are stationary.
	- State: S
	- Model: T(s,a,s')~ Pr(s'|a,s')
		- A transition model describes: the **rules** of the game that you are playing in the **physics of the world**.
		- The T function prduces the probability that you will end up trasitioning the state s', given that you were in state s and you took action a.
	- Actions: A(s), A 
		- up, down, left, right
	- Reward: **R(s)**, R(s,a), R(s,a,s')
		- Reward is a scalar value that you get for being in a state.
	- Policy:
		- The above describes a problem, and **policy** is the solution.
		- π(s) → a (what policy does is: it's a function that takes in a state, and returns an action.)
		- π* (optimal policy: the policy that maximize your long-term expected reward.)
	- ![p4](https://raw.githubusercontent.com/suereey/RL_CS7642_Fall2021_StudyNotes/main/screenshot/P1_04.PNG)

## MDPs: More about Reward
- Delayed reward
	- ![p5](https://raw.githubusercontent.com/suereey/RL_CS7642_Fall2021_StudyNotes/main/screenshot/P1_05.PNG)
- Minor changes matter: the value of R(s) matters.
	- ![p6](https://raw.githubusercontent.com/suereey/RL_CS7642_Fall2021_StudyNotes/main/screenshot/P1_06.PNG)

## Sequnce of reward: assmptions
- ![p7](https://raw.githubusercontent.com/suereey/RL_CS7642_Fall2021_StudyNotes/main/screenshot/P1_07.PNG)
- ![p8](https://raw.githubusercontent.com/suereey/RL_CS7642_Fall2021_StudyNotes/main/screenshot/P1_08.PNG)
- ![p9](https://raw.githubusercontent.com/suereey/RL_CS7642_Fall2021_StudyNotes/main/screenshot/P1_09.PNG)
## Assumptions
- ![p10](https://raw.githubusercontent.com/suereey/RL_CS7642_Fall2021_StudyNotes/main/screenshot/P1_10.PNG)

## Policies (important)
- Bellman equation
	- **π***, the optimum policy : is the one that maximizes the long term simplified reward.
	- **Uπ(s)**, Utility of a particular state depend upon the followed policy : is going to be the expected set of states that we are going to see from that point on, give that it follows the policy.
	- Utility != Reward
		- Reward: immediate feedback
		- Utility: longterm feedback (all the reward from that point)
	- **π*(s)**, the optimum policy is the one that at every state, returns the action that maximizes my expected utility
	- U(s) the true utility of a state is the reward that I get for being in tha tstate **+** discount (**γ**) times the reward that we get from that point on.
	- ![p11](https://raw.githubusercontent.com/suereey/RL_CS7642_Fall2021_StudyNotes/main/screenshot/P1_11.PNG)
		- for the bellman equation: **n** states, so **n** equations with **n** unkonws. To get U(s), if the quation is linear, then can be easily solved. However, the **maximum function** involves nonlinear.
		- Solutions:
			- start with arbitrary utilities
			- update based on neighbours
			- repeat utility convergence
			- ![p12](https://raw.githubusercontent.com/suereey/RL_CS7642_Fall2021_StudyNotes/main/screenshot/P1_12.PNG)
			- explain th equation: will update the utility of s by looking at the utilities of all the other states, including itself, s'. And weight those based on the probablity to getting there given that I took an action.  

	- Quiz
		- ![p13](https://raw.githubusercontent.com/suereey/RL_CS7642_Fall2021_StudyNotes/main/screenshot/P1_13.PNG)
	- Find policies: the udpated eqn changed the nonlinear problem into linear.
		- ![p14](https://raw.githubusercontent.com/suereey/RL_CS7642_Fall2021_StudyNotes/main/screenshot/P1_14.PNG)
## Bellman Eqn
- Different bellman eqns:
	- ![p15](https://raw.githubusercontent.com/suereey/RL_CS7642_Fall2021_StudyNotes/main/screenshot/P1_15.PNG)
	- ![p16](https://raw.githubusercontent.com/suereey/RL_CS7642_Fall2021_StudyNotes/main/screenshot/P1_16.PNG)
	- ![p17](https://raw.githubusercontent.com/suereey/RL_CS7642_Fall2021_StudyNotes/main/screenshot/P1_17.PNG)
- Relationships:
	- ![p18](https://raw.githubusercontent.com/suereey/RL_CS7642_Fall2021_StudyNotes/main/screenshot/P1_18.PNG)

## Summary
- ![p19](https://raw.githubusercontent.com/suereey/RL_CS7642_Fall2021_StudyNotes/main/screenshot/P1_19.PNG)