# TD and Friends
## 3 main families of reinforcement learning algorithms
- Model based:
    - model based RL algorithms takes the state action reward tuples, sends them to a model learner, which learns the traisitions and rewards. Once it learn T/R, put them into MDPSolver, which could be used to spit out a Q* (a optimal value function). Once you have the optimal value function you can use choose what action you should take in any give state and that gives you the policy.
- Value function based (model free):
    - Instead of feeding back the transition and reward, we feed back the Q*. And we have a direct value update equation that takes state action reward that it just experienced, the current estimate of Q*.
- Policy search
![01]()
## TD Lambda (temperal difference learning)
- Learning to predict over time:
    ![02]()
- Example:
    - ![03]()
    - Calculatge V(S3)