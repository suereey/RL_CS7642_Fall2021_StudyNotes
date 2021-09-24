# TD and Friends
## 3 main families of reinforcement learning algorithms
- Model based:
    - model based RL algorithms takes the state action reward tuples, sends them to a model learner, which learns the traisitions and rewards. Once it learn T/R, put them into MDPSolver, which could be used to spit out a Q* (a optimal value function). Once you have the optimal value function you can use choose what action you should take in any give state and that gives you the policy.
- Value function based (model free):
    - Instead of feeding back the transition and reward, we feed back the Q*. And we have a direct value update equation that takes state action reward that it just experienced, the current estimate of Q*.
- Policy search
![01](https://raw.githubusercontent.com/suereey/RL_CS7642_Fall2021_StudyNotes/main/screenshot/L3/01_RLContext.PNG)
## TD Lambda (temperal difference learning)
- Learning to predict over time:
    ![02](https://raw.githubusercontent.com/suereey/RL_CS7642_Fall2021_StudyNotes/main/screenshot/L3/02.PNG)
- Example 01:
    - ![03](https://raw.githubusercontent.com/suereey/RL_CS7642_Fall2021_StudyNotes/main/screenshot/L3/03_example.PNG)
    - Calculatge V(S3)
        - V(S3) = 0.9(probability of V4) * 1 (reward of v4) * γ + 0.1(p of v5) * 10 (r of v5) * γ = 1.9 * γ
        - when γ=1, V(S3) = 1
- Example 02: Estimate from data
    - Simple way:
    ![5a](https://raw.githubusercontent.com/suereey/RL_CS7642_Fall2021_StudyNotes/main/screenshot/L3/5a.PNG)
    - Generalize it:
    ![5b](https://raw.githubusercontent.com/suereey/RL_CS7642_Fall2021_StudyNotes/main/screenshot/L3/5b.PNG)
        - Looking at the temperal difference () and update to the value is going to equal to the difference between the reward (current step), and the estimated we have in the previous step. This difference drives the learning.
        - Similar as perceptron, in that way, the term in () is the error term in perceptron.
- Select learning rate:
    - If learning rate dosen't get smaller overtime, it would never converge
    - ![06](https://raw.githubusercontent.com/suereey/RL_CS7642_Fall2021_StudyNotes/main/screenshot/L3/6.PNG)
## TD Rule and Examples
- TD(1):
    - ![07](https://raw.githubusercontent.com/suereey/RL_CS7642_Fall2021_StudyNotes/main/screenshot/L3/07.PNG)
    - ![08](https://raw.githubusercontent.com/suereey/RL_CS7642_Fall2021_StudyNotes/main/screenshot/L3/08.PNG)
- TD(0):
    - ![09](https://raw.githubusercontent.com/suereey/RL_CS7642_Fall2021_StudyNotes/main/screenshot/L3/09.PNG)
- TD Lambda:
    - ![10](https://raw.githubusercontent.com/suereey/RL_CS7642_Fall2021_StudyNotes/main/screenshot/L3/10.PNGs)
- K step estimator
    - ![11](https://raw.githubusercontent.com/suereey/RL_CS7642_Fall2021_StudyNotes/main/screenshot/L3/11.PNG)
    - ![12](https://raw.githubusercontent.com/suereey/RL_CS7642_Fall2021_StudyNotes/main/screenshot/L3/12.PNG)
    - ![13](https://raw.githubusercontent.com/suereey/RL_CS7642_Fall2021_StudyNotes/main/screenshot/L3/13.PNG)
## Summary
![14](https://raw.githubusercontent.com/suereey/RL_CS7642_Fall2021_StudyNotes/main/screenshot/P1_14.PNG)
