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

# Exploitation and Explotation

MC control with e-greedy PI

샘플을 사용하기 때문에.

# SARSA  using TD Control
on policy.

q learning 과의 차이점.

sample된 action에 대한 value function으로 update
가장 좋은 action에 대한 value function으로 update (q)

# Policy Gradient
주어진 상태에 모든 액션들의 선택적 확률 분포도가 얼마나 좋은지 목적 함수를 설계해, 함수를 최대화 하는 방향으로 액션 선택.

# Policy Parametrization
정책의 평가를 목적함수를 사용.

local optimal problem

# Reinforce : MC 기반한 방법
Approximation Q

# Actor-Critic
TD update.
actor : policy update.

# Deep Reinforcement Learning

DL이 RL에 적용되는 문제들 : state가 무한대에 가까운 문제.

# DQN

state : images

action : control

reward : score

# Replay Buffer

high correlation sample.
make replay buffer(memory)

# Moving Target

terget과 같은 내트워크로 업데이터를 하기 때문에 타겟이 흔들린다.

네트워크를 2개로 분리.

# Structure of DQN

CNN + fully connected = control

# High action space
DQN을 로봇과 같은 액션이 많은 환경에서 사용할 수 없는 이유:

high complexity action.

연속적(많은) 액션의 가치를 추정하는 함수가 수행시 오래 걸림.

복잡한 action space에서 q 가치함수의 형태가 복잡함.

Low sample efficiency.


# Policy Gradient Method

Actor-critic method.

DNN + AC

# DDPG

Actor / Critic 함수를 네트워크로 교체.

Actor는 policy를 업데이트. Critic은 policy를 평가.

+Deterministic policy (제어 환경에서 환경은 쉽게 변화하지 않음)

Deterministic policy : u 특정 상태에서 특정 액션을 취함.

# On or Off Policy , Buffer

Off Policy : replay buffer. (sample correlation delete)

Target network : actor / critic 

E greedy 방법 -> action noise.



