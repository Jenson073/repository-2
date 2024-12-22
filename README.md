# 📈 **Trading Environment with Q-Learning**

This project demonstrates a **Q-Learning** agent applied to a custom trading environment where the agent learns to make trading decisions based on stock price data. The agent can perform three actions: **Buy**, **Sell**, or **Hold**. The goal is for the agent to maximize its profit over time.

The environment is created using the **OpenAI Gym** framework, where the state of the environment is the current stock price, and the reward is based on the total profit accumulated from the trading actions. The Q-learning algorithm is employed to train the agent to make optimal decisions.

---

## 🌟 **Features**  

- **Custom Trading Environment**:  
  - Actions: **Hold**, **Buy**, **Sell**.  
  - State: The **stock price** at the current time step.  
  - Reward: Based on the **profit** (total balance - initial balance).

- **Q-Learning Algorithm**:  
  - Epsilon-Greedy exploration strategy to balance exploration and exploitation.  
  - The Q-table is updated using the **Bellman Equation**.  
  - Learning rate (`alpha`), discount factor (`gamma`), and epsilon decay rate to control the learning process.

---

## 🧠 **Q-Learning Details**  

- **State Space**:  
  - The state space is represented by the **current stock price**, where the agent’s state is a continuous value. For simplicity, the state is clipped to integers between 0 and 999.

- **Action Space**:  
  - **0**: **Hold** – Do nothing.  
  - **1**: **Buy** – Buy one share of the stock.  
  - **2**: **Sell** – Sell one share of the stock.

- **Q-Table**:  
  - The Q-table holds the learned Q-values for each state-action pair.  
  - The agent updates the Q-table using the **Q-value update rule**.

---

## ⚙️ **Parameters**  

| Parameter            | Value        | Description                               |
|----------------------|--------------|-------------------------------------------|
| **Episodes**          | 1000         | Number of episodes to train the agent.    |
| **Learning Rate**     | 0.1          | The rate at which the model learns.       |
| **Discount Factor**   | 0.99         | The discount factor for future rewards.   |
| **Epsilon**           | 1.0 (decays) | Initial exploration rate (epsilon-greedy).|
| **Epsilon Decay**     | 0.995        | Decay rate for epsilon over time.        |
| **Epsilon Min**       | 0.01         | Minimum epsilon value.                   |

---

## 📊 **Results**  

- **Total Profit Over Episodes**: The agent learns to make profitable decisions based on past actions and stock prices. The total profit for each episode is plotted to visualize the agent’s performance.
- **Epsilon Decay**: The epsilon value decreases as training progresses, allowing the agent to explore less and exploit more as it learns.
  
The following plot is generated at the end of training, showing the **total profit** over all episodes:

---

## 🔧 **How to Run the Code**  

1. **Install Dependencies**:  
   Ensure you have Python installed along with the required libraries:  
   ```bash
   pip install gym numpy pandas matplotlib

---
