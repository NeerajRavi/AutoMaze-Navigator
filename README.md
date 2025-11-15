<!--
  AutoMaze Navigator - README (HTML)
  Copy & paste the entire contents below into your README.md on GitHub.
  GitHub renders inline HTML inside Markdown files.
-->

<div align="center" style="margin-bottom:18px;">
  <h1 style="font-size:38px; margin:6px 0;"><strong>AutoMaze Navigator</strong></h1>
  <p style="font-size:16px; margin:0;">
    <strong>DFS Maze Generator + Q-Learning Solver</strong> — a dynamic maze-generation and reinforcement-learning navigation system built in Python.
  </p>
  <p style="font-size:14px; color:#666; margin-top:6px;">
    Developed by <strong>Neeraj Ravi P V</strong>
  </p>
</div>

<hr />

<section>
  <h2 style="font-size:22px; margin-top:12px;">Overview</h2>
  <p style="font-size:15px; line-height:1.5;">
    <strong>AutoMaze Navigator</strong> is an end-to-end Python project that combines classic algorithms and Reinforcement Learning:
  </p>
  <ul style="font-size:15px; line-height:1.6;">
    <li>Generates a random maze using <strong>Iterative DFS</strong></li>
    <li>Computes the shortest path using <strong>Breadth-First Search (BFS)</strong></li>
    <li>Adds randomized internal wall removals and dynamic obstacles</li>
    <li>Trains a <strong>Q-Learning</strong> agent to find efficient paths</li>
    <li>Visualizes the maze and learned RL path using Matplotlib</li>
  </ul>
</section>

<hr />

<section>
  <h2 style="font-size:22px; margin-top:12px;">Objectives</h2>
  <ul style="font-size:15px; line-height:1.6;">
    <li>Generate unique, solvable mazes every run</li>
    <li>Guarantee a ground-truth shortest path (BFS)</li>
    <li>Increase challenge with random walls & obstacles</li>
    <li>Train a Q-Learning agent to navigate efficiently</li>
    <li>Provide clean visualizations</li>
  </ul>
</section>

<hr />

<section>
  <h2 style="font-size:22px; margin-top:12px;">Key Features</h2>

  <h3 style="font-size:18px; margin:10px 0 6px 0;">Random Maze Generator (Iterative DFS)</h3>
  <p style="font-size:15px; line-height:1.5;">
    Produces a perfect maze (single unique path between two cells), ensuring full connectivity and solvability.
  </p>

  <h3 style="font-size:18px; margin:10px 0 6px 0;">BFS Shortest Path</h3>
  <p style="font-size:15px; line-height:1.5;">
    Computes the guaranteed shortest path from the start to the goal — used as a benchmark for RL training and reward shaping.
  </p>

  <h3 style="font-size:18px; margin:10px 0 6px 0;">Internal Wall Removal & Obstacles</h3>
  <p style="font-size:15px; line-height:1.5;">
    Randomly removes internal walls (borders preserved) and places obstacles that do not overlap the BFS path, start, or end points — increasing complexity for the agent.
  </p>

  <h3 style="font-size:18px; margin:10px 0 6px 0;">Q-Learning Agent</h3>
  <p style="font-size:15px; line-height:1.5;">
    Discrete actions (UP, DOWN, LEFT, RIGHT). Rewards include:
  </p>
  <ul style="font-size:15px; line-height:1.6;">
    <li>Positive reward for reaching the goal</li>
    <li>Negative reward for invalid moves / hitting walls / obstacles</li>
    <li>Small step penalty to encourage efficient paths</li>
    <li>Optional shaping reward when following BFS route</li>
  </ul>

  <h3 style="font-size:18px; margin:10px 0 6px 0;">Visualization</h3>
  <p style="font-size:15px; line-height:1.5;">
    Matplotlib-based renderings: maze layout, BFS overlay, agent trajectory, and training/reward plots.
  </p>
</section>

<hr />

<section>
  <h2 style="font-size:22px; margin-top:12px;">Algorithms Used</h2>
  <table style="border-collapse:collapse; width:100%; font-size:15px;">
    <thead>
      <tr>
        <th style="text-align:left; padding:8px; border-bottom:1px solid #ddd;">Algorithm</th>
        <th style="text-align:left; padding:8px; border-bottom:1px solid #ddd;">Purpose</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td style="padding:8px; border-bottom:1px solid #f3f3f3;"><strong>Iterative DFS</strong></td>
        <td style="padding:8px; border-bottom:1px solid #f3f3f3;">Maze generation (carving paths)</td>
      </tr>
      <tr>
        <td style="padding:8px; border-bottom:1px solid #f3f3f3;"><strong>BFS</strong></td>
        <td style="padding:8px; border-bottom:1px solid #f3f3f3;">Shortest-path computation</td>
      </tr>
      <tr>
        <td style="padding:8px;"><strong>Q-Learning</strong></td>
        <td style="padding:8px;">Reinforcement Learning for navigation</td>
      </tr>
    </tbody>
  </table>
</section>

<hr />

<section>
  <h2 style="font-size:22px; margin-top:12px;">Project Workflow</h2>
  <ol style="font-size:15px; line-height:1.6;">
    <li>Initialize grid with walls</li>
    <li>Generate maze using Iterative DFS</li>
    <li>Compute BFS shortest path</li>
    <li>Remove random internal walls; add obstacles</li>
    <li>Train Q-Learning agent (episodes & exploration)</li>
    <li>Visualize learned path</li>
  </ol>
</section>

<hr />

<section>
  <h2 style="font-size:22px; margin-top:12px;">Project Structure</h2>

  <pre style="background:#f7f7f7; padding:12px; border-radius:6px; font-size:14px; overflow:auto;">
AutoMazeNavigator/
│
├── images/                # Folder containing all visualization images
│   ├── maze_example.png   # Maze visualization
│   └── maze_with_path.png # Q-learning agent path (optional)
│
├── notebook/              # Jupyter notebooks
│   └── maze.ipynb         # Notebook demonstrating maze generation & Q-learning
│
├── requirements.txt       # Python dependencies
│
└── README.md              # Project documentation
  </pre>
</section>

<hr />

<section>
  <h2 style="font-size:22px; margin-top:12px;">Installation & Setup</h2>

  <h3 style="font-size:16px; margin-bottom:6px;">Clone the repository</h3>
  <pre style="background:#f7f7f7; padding:10px; border-radius:6px; font-size:14px;">git clone https://github.com/NeerajRavi/AutoMazeNavigator
cd AutoMazeNavigator</pre>

  <h3 style="font-size:16px; margin-bottom:6px;">Install dependencies</h3>
  <pre style="background:#f7f7f7; padding:10px; border-radius:6px; font-size:14px;">pip install -r requirements.txt</pre>

  <h3 style="font-size:16px; margin-bottom:6px;">Run the notebook</h3>
  <pre style="background:#f7f7f7; padding:10px; border-radius:6px; font-size:14px;">jupyter notebook notebook/Maze.ipynb</pre>

  <p style="font-size:15px; color:#444;">
    <strong>Expected console messages:</strong><br />
    <em>Maze Generated Successfully!</em><br />
    <em>BFS Shortest Path Found</em><br />
    <em>Agent Learned Optimal Path!</em>
  </p>
</section>

<hr />

<section>
  <h2 style="font-size:22px; margin-top:12px;">Requirements</h2>
  <ul style="font-size:15px; line-height:1.6;">
    <li>Python 3.8+</li>
    <li>numpy</li>
    <li>matplotlib</li>
    <li>(builtin) random, collections</li>
  </ul>
</section>

<section>
  <h2 style="font-size:22px; margin-top:12px;">Learning Outcomes</h2>
  <ul style="font-size:15px; line-height:1.6;">
    <li>Implement Iterative DFS for maze generation</li>
    <li>Compute BFS for guaranteed shortest-path solutions</li>
    <li>Understand Q-Learning mechanics (states, actions, rewards, Q-table)</li>
    <li>Design reward shaping and training loops</li>
    <li>Visualize algorithmic outputs with Matplotlib</li>
  </ul>
</section>

<hr />

<section>
  <h2 style="font-size:22px; margin-top:12px;">Future Enhancements</h2>
  <ul style="font-size:15px; line-height:1.6;">
    <li>Deep Q-Network (DQN) support for larger mazes</li>
    <li>Epsilon-decay and advanced exploration strategies</li>
    <li>Animated training GIFs and interactive visualizations</li>
    <li>PyGame-based GUI for manual play & demonstration</li>
    <li>Multi-agent or adversarial maze setups</li>
  </ul>
</section>

<!-- End of README HTML -->