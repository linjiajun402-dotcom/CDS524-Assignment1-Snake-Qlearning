# CDS524 Assignment 1 — Q-learning Snake (Snake Game Reinforcement Learning)

This project implements a grid-based Snake game and uses **Q-learning** to train the agent to learn how to "eat food and try to survive."

The project includes training logs, Q-table output, and pygame UI demo animations/videos.


## 1. Project Files (Submission Files)

- `CDS524_Assignment1_Lin.ipynb`: Main code (recommended to run on Google Colab)

- `report.pdf`: Assignment report

- `snake_demo.gif`: Animated demonstration of the greedy policy after training

- `snake_demo.mp4`: Video demonstration of the greedy policy after training

- `q_table.csv`: Q-table (state-action value table) obtained after training

- `train_log.csv`: Training log (episode reward / steps / score)


## 2. Game Rules

- The map is an N×N grid (default 12×12)

- Actions control the snake's movement: Each step moves the snake one square forward

Eating food: The snake grows longer and receives a reward

Hitting a wall or hitting itself: Game over (terminates)


## 3. Reinforcement Learning Design (RL) Design

### State
State is represented using discrete features:

- `danger_ahead / danger_left / danger_right`: Is the front/left/right direction dangerous (0/1)

- `food_dir_x / food_dir_y`: Food direction relative to the snake's head (-1/0/1)

- `current_dir`: Current direction (UP/RIGHT/DOWN/LEFT)

### Action
Action is represented using relative actions (3 classes):

- `TURN_LEFT` / `STRAIGHT` / `TURN_RIGHT`

### Reward

- Eat food: `+1`

- Die: `-1`

- Per step: `-0.01` (Encourages more efficient food searching)

### Q-learning Update

\[ Q(s,a) \leftarrow Q(s,a) + \alpha (r + \gamma `\max_{a'}Q(s',a') - Q(s,a))



## 4. How to Run

Recommended to use **Google Colab**:

1. Open `CDS524_Assignment1_Lin.ipynb`

2. Run all cells from top to bottom (automatically installs dependencies and trains the model)

3. After training, demo files `snake_demo.gif` / `snake_demo.mp4` will be generated.

Dependencies (installed within the notebook):

- `pygame`

- `numpy`

- `matplotlib`

- `pandas`

- `imageio` / `imageio-ffmpeg`



## 5. Demo

- Animated GIF: `snake_demo.gif`

- Video: `snake_demo.mp4`

- (If you need a YouTube link, please paste it here)

- YouTube Demo: <YOUR_LINK_HERE>



## 6. Author
Lin Jiajun
