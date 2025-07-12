# Space_Invaders
A multi-agent deep reinforcement learning project exploring cooperation and competition in Atari Space Invaders using Independent and Shared DQNs.

# Multiagent Reinforcement Learning in Space Invaders

This project explores emergent cooperation and competition in a multi-agent setting using Deep Q-Networks (DQNs) in the Atari Space Invaders environment, implemented via the PettingZoo library. It compares two architectures:

- **Independent DQN (IDQN)**: Each agent has its own neural network and replay buffer.
- **Shared DQN (SDQN)**: A single shared network governs the behavior of both agents.

## 🧠 Project Structure

- `space_invaders_independent_dqn.ipynb` — Main implementation and training using Independent DQNs
- `space_invaders_shared_dqn.ipynb` — Baseline using a shared DQN across both agents
- Recorded gameplay videos
- Generated visualizations of agent behavior and cooperation metrics

## 📦 Dependencies

To run this project, install the following Python packages:

```bash
pip install pettingzoo[atari] supersuit pygame imageio matplotlib torch
```

For training and video generation, we recommend using **Google Colab** with GPU enabled.

## 🎮 ROM Setup

PettingZoo requires installation of Atari ROMs. Run this once to install:

```bash
AutoROM --accept-license
```

This will install ROMs for all Atari environments, including Space Invaders.

## 🚀 How to Run

1. **Colab Setup**  
   Upload the desired notebook (`independent_dqn` or `shared_dqn`) to [Google Colab](https://colab.research.google.com/).

2. **Enable GPU**  
   Runtime → Change runtime type → Select **GPU**

3. **Install Dependencies (first cell)**  
   Run the setup cell to install required packages.

4. **Train Agents**  
   Execute all cells. Training will take ~30 minutes depending on the number of episodes.

5. **View Results**  
   The notebook logs reward scores, cooperation index, sabotage events, and produces:
   - Learning curve plots
   - Cooperation vs. competition metrics
   - Recorded gameplay videos (MP4)

## 📊 Evaluation Metrics Tracked

- **Reward per episode** (per agent)
- **Cooperation Index**: measures score similarity
- **Bonus Events**: counts +200 sabotage bonuses
- **Shots Fired / Kills / Coexistence Time**

## 📂 Output Files

- `agent_play.mp4` — Sample of trained agents playing
- Visual comparison of strategies

## 📌 Notes

- Trained for 35 episodes due to compute constraints.
- For longer training, increase `NUM_EPISODES` and reduce `RENDER_INTERVAL`.

## 🧾 Reference

Based on:
- [Tampuu et al., 2017] Multiagent Cooperation and Competition with Deep RL (PLoS One)
- Mnih et al., 2015 (Nature) — Original DQN paper
- PettingZoo & Supersuit documentation

---

For questions, refer to our full paper or reach out to the authors.

Team: Chanakya Nalapareddy, Khushboo Patel, Uday Pothuri.

Drexel University — Spring 2025
