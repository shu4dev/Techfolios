---
layout: project
type: project
image: img/proteinfolding.jpg
title: "Protein Folding"
date: 2022
published: true
labels:
  - Python
  - WebDriver
summary: "A script that find the best way the fold protein"
---
# Introduction
This Python script is dedicated to a research project during the summer. The goal of this project is to find the best way to fold proteins by using a hydrophobic-polar protein folding model. My group mates and I utilize Python and algorithms to assist in this project to find the optimal protein folding solution. 

# hydrophobic-polar protein folding model

In simple terms, this model is a string that contains 0s and 1s. Between each number, they are connected, and the change in the direction of the next number is considered a fold.

In order to score, the following condition must be satisfied:

1. The number must be next to each other without a connection
2. Both number must be 0

# Code

To achieve this goal, we use recursive backtracking.
```python
def ProteinFolding(Acidseq, grid, Curnum, y, x, pts, resgrid):
    global Maxpts
    global y_move
    global x_move
    global direc
    if Curnum == len(Acidseq):
        if pts > Maxpts:
            Maxpts = pts
            CopyArray(grid, resgrid, len(grid))
        return resgrid
    
    for i in range(4):
        
        y_prog = y + y_move[i]
        x_prog = x + x_move[i]
        
        y_new = y_prog + y_move[i]
        x_new = x_prog + x_move[i]

        if isValid(grid, y_new, x_new):

            grid[y_prog][x_prog] = symbol[i]
            grid[y_new][x_new] = Acidseq[Curnum]
            pts_new = pts + Checkpts(grid, y_new, x_new, direc[i])
            CopyArray(resgrid, ProteinFolding(Acidseq, grid, Curnum + 1, y_new, x_new, pts_new, resgrid), len(grid))
            grid[y_new][x_new] = " "
            grid[y_prog][x_prog] = " "

    return resgrid
```

Source: <a href="https://github.com/shu4dev/ProteinFolding"><i class="large github icon "></i>Protein Folding</a>
