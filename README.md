# 🧩 Interactive AI Maze Path-Finder (BFS)

**Course:** Fundamentals of AI (CF321) – Innovation University
**Team:** [Rawan Tamer - 24030140], 

[

![Open In Colab]
]([https://colab.research.google.com/drive/1qQFXtZtptk3cZXBGlZNvdNm4oZLHWYaH#scrollTo=z5izMyIYG38a)

## 💡 Idea
An intelligent agent that navigates an 8×8 grid maze from a start cell to a goal cell using **Breadth-First Search (BFS)**. Instead of typing coordinates in a console, the user works with an **interactive dashboard** inside Google Colab: pick the start and goal from dropdowns, see a live preview of the maze, and press **Solve**. The search is then shown as an **animation**: the BFS wave expands cell by cell, and finally the shortest path is highlighted.

## 📝 Problem Definition
| Element | Definition |
|---|---|
| **States** | Grid coordinates `(row, col)` of the agent in the 8×8 maze |
| **Initial State** | Chosen by the user from the dropdowns |
| **Goal State** | Chosen by the user from the dropdowns |
| **Actions** | Up `(-1,0)`, Down `(1,0)`, Left `(0,-1)`, Right `(0,1)` |
| **Action Cost** | Uniform, 1 per move |
| **Walls** | Cells with value `1` cannot be entered |

## 🔍 Algorithm: Breadth-First Search (BFS)
BFS explores the maze level by level using a queue (`collections.deque`). A `parent` dictionary works as both the visited set (prevents cycles and repeated work) and the record used to rebuild the path from the goal back to the start.

**Why BFS?** Every move costs 1 (an unweighted graph), so BFS is **complete and optimal**: it always finds a path if one exists, and that path is the shortest. Time and space complexity are O(V + E), which is tiny for an 8×8 grid.

## ✨ Features
- 🎛️ **Interactive dashboard** (ipywidgets): dropdowns for start/goal and a **Solve with BFS** button.
- 👀 **Live preview**: the maze redraws instantly with `S` and `G` whenever a selection changes.
- ✅ **Input validation**: shows an error and disables the button if the start or goal is a wall, or if goal = start.
- 🎞️ **Search animation**: explored cells in blue, then the shortest path in yellow.
- ⏱️ **Speed slider** to control the animation speed.
- 📊 **Result cards** for Solution Status, Solution Cost, and Search Cost.
- 🔤 **Text rendering** of the final maze: `S` start, `G` goal, `*` path, `█` wall, `.` open cell.

## 📊 Output Metrics
- **Solution Status:** whether a path was found.
- **Solution Cost:** number of steps in the shortest path.
- **Search Cost:** number of nodes explored by BFS.

Example: start `(0,0)` → goal `(7,7)` gives a solution cost of **14 steps**.

## ▶️ How to Run
1. Click the **Open in Colab** badge above (or open `maze_bfs.ipynb` and press *Open in Colab*).
2. Run the code cell: **Runtime → Run all**.
3. Choose the **START** and **GOAL** cells from the dropdowns (Row and Col, 0–7).
4. Optionally adjust the **Speed** slider.
5. Press **Solve with BFS** and watch the results and the animation. Press ▶ on the animation if it does not start automatically.

**Requirements:** Python 3, `matplotlib`, `ipywidgets` (both are pre-installed on Google Colab).

> ⚠️ The interactive dashboard and animation work inside Google Colab / Jupyter only. GitHub shows the code but does not run the widgets.

## 🖼️ Screenshots
[PASTE SCREENSHOT OF THE DASHBOARD HERE]

[PASTE SCREENSHOT OF THE ANIMATION / RESULTS HERE]

## 🗺️ Maze Layout (0 = open, 1 = wall)
```
0 0 0 1 0 0 0 0
1 1 0 1 0 1 1 0
0 0 0 0 0 0 1 0
0 1 1 1 1 0 1 0
0 0 0 0 1 0 0 0
1 1 1 0 1 1 1 0
0 0 0 0 0 0 1 0
0 1 1 1 1 0 0 0
```

## 👥 Team
- [Rawan Tamer ]-[ 24030140]
  
