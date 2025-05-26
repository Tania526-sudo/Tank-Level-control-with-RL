# Tank Level Control with Reinforcement Learning

This project implements classical and temporal difference (TD) reinforcement learning algorithms to control the water level in a tank using simulation-based methods.

## Key ideas:

1) A Q-learning agent is trained to control the water level in a tank by minimizing the deviation from a dynamic setpoint.

2) The system state is discretized into finite levels to fit a Q(s, a) table structure.

3) The training process uses ε-greedy policy and updates the setpoint periodically.

4) The reward function encourages convergence to the setpoint and penalizes deviation:
reward = 100 if S == Sp else -np.square(S - Sp) * 100

5) After training, the agent is evaluated with randomly changing setpoints. It shows stable behavior and a responsive control policy.

Results:
The tank level h converges to the target Set point over time.
The input flow is applied in short bursts, only when needed.

GitHub repository includes:

Full standalone Python code (no external imports required)

Jupyter notebook for simulation and visualization

Plotting of agent performance and system response

MATLAB equivalent model for comparison