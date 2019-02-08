# MDP
env modeling.

# Policy
현재 state에서 취할 수 잇는 모든 action의 확률.

Good policy : 감가율이 적용된 보상의 합을 maximize 하는 것.

# Value Functions

### 1. State value function
현재 state에서 policy를 따라서 수행했을 때 얻는 보상 합의 기댓 값 
현재 state에 대해서 평가한다.
### 2. Action value function
현재 state에서 특정 action을 수행했을 때 얻는 보상 합의 기댓 값

특정 action에 대해서 평가한다.


# Optimal Value and Policy

Optimal policy : 주어진 state에서 action value function 을 최대화 하는 action을 선택.

optimal value function을 최대화 하는 action으로 policy를 구성하면 optimal 중 하나.

# Dynamic programming
### 1. Prediction
policy를 평가

Input : MDP , Policy

Output : value function

### 2. Control
Input : MDP

Output : Optimal policy

Bellman Equation : Policy linear equation 

# Policy Iteration

Loop policy evaluation and policy improvement

improvement :  p' > p

# Policy Improvement 
if Q(s,a)[action을 수행 후 모든 보상] > V(s)[모든 action의 확률 모든 보상]

    action select.

# Value Iteration
Bellman optimal equaltion

value function -> optimal policy X

max value function.

# Model Free RL

MDP가 주어지지 않았을 경우 (s, a, r ,s')의 샘플을 통해서 추측

# Model Free Prediction

### 1. Monte Carlo policy evaluation
현재 state를 평가하기 위해 수 많은 action 을 수행해서 평균 return.

경험적 평균.

샘플을 많이 수집했을 경우 수렴 보장.

#### Expressing Mean Incremmentally

### 2. Temporal-difference learning

스탭 단위의 알고리즘.

Bootstrapping.

마지막 return 을 기다리지 않고 매 스탭마다 online으로 업데이트.

서로 독립적인 샘플들을 수 많이 수집하였을 때 수렴 보장. (sarsa)

# Bias-Variance Trade-off

MC : no bias. variance 가 높음.
TD : high bias. variance 가 낮음. 




