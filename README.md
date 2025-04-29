# Super Mario Bros AI Agent 🎮🧠

This project explores the application of **Reinforcement Learning (RL)** and **Computer Vision** techniques to train an agent capable of completing a level of the classic *Super Mario Bros* game. It was developed for the Artificial Intelligence course at the University of Salerno.

---

## 📌 Project Summary

Three main approaches were tested:

1. **DDQN** (Deep Double Q-Network)
2. **PPO** (Proximal Policy Optimization) with different configurations
3. **PPO + YOLOv5** integration for object detection

The agent was trained to complete the level `SuperMarioBros-1-1-v0` using `gym-super-mario-bros`.

---

## 🧠 Objectives

- Train an agent to autonomously complete a level of Super Mario Bros
- Compare RL models (DDQN vs PPO)
- Improve vision-based decisions with **YOLOv5** object detection
- Analyze performance through metrics like reward, Q-values, and policy loss

---

## 📁 Project Structure

```bash
.
├── docs/                       # Project documentation
│   ├── Traccia.pdf             # Project prompt
│   ├── Relazione Super Mario Bros.pdf   # Final report
│   └── Presentazione Super Mario.pptx   # Presentation slides
│
├── media/                      # Output media
│   ├── completo.mp4            # Full run demo
│   └── Vittoria_Mario.mp4      # Winning episode clip ✅
│
├── prog/                       # Code and notebooks
│   ├── ddqn_agent.py           # DDQN implementation (PyTorch)
│   ├── ppo_512_batch.ipynb     # PPO with 512 steps
│   ├── ppo_2048_batch.ipynb    # PPO with 2048 steps
│   ├── ppo_with_yolo.ipynb    # PPO + YOLOv5 integration
│   └── mario_env/              # Ignored virtual environment
│
├── .gitignore                  # Excludes `mario_env`
└── README.md                   # You're here
```

---

## 🛠️ Technologies Used

- Python 3, PyTorch, OpenCV
- Stable-Baselines3 (PPO)
- YOLOv5 (Roboflow + Ultralytics)
- gym-super-mario-bros
- Custom wrappers (frame stack, reward shaping)

---

## 🎯 Key Results

| Model           | Victories         | Notes |
|----------------|-------------------|-------|
| DDQN           | 1/1000 episodes   | High stability |
| PPO (512 steps)| 54/10M steps      | Best result overall |
| PPO (2048)     | 0                 | Failed to converge |
| PPO + YOLOv5   | 0                 | Better perception, poor translation to actions |

YOLOv5 achieved **94.2% precision** and **100% recall**, but the integrated agent still failed to win due to difficulty performing complex jumps.

---

## 🎮 Gameplay Demo

<p align="center">
    <img src="https://github.com/Marco210210/SuperMario-RL-DDQN-PPO-YOLOv5/blob/main/media/Demo_Mario.gif" width="400">
</p>

---

## 🎥 Demo Video

Watch the agent win!  
📹 [Victory Clip](media/Vittoria_Mario.mp4)

Or check the full episode:  
📺 [Full Demo](media/completo.mp4)

---

## 📌 Notes

- This project required significant hardware resources (GPU for training PPO/YOLOv5).
- Training time: ~48h for PPO + YOLOv5 on Mac without GPU.
- All models trained on `SuperMarioBros-1-1-v0`.

---

## 👥 Authors

- Giovanni Arcangeli  
- Vittorio Ciancio  
- Marco Di Maio  

---

## 📬 Contact

For questions or feedback, feel free to reach out via GitHub or email.

