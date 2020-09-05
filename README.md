# Conway's Reverse Game of Life 2020 - Genetic Algorithm

This repository contains the approach of solving the [challenge](https://www.kaggle.com/c/conways-reverse-game-of-life-2020) posted on Kaggle. The whole algorithm is described on [Medium](https://medium.com/@ptyshevs/rgol-ga-1cafc67db6c7) in great detail. You can find accompanying code in `ga_tutorial.ipynb`.

Almost equivalent code is used in `GeneticSolver`, with multiprocessing version of fitness scoring added. `MPGeneticSolver` goes one step further by running multiple `GeneticSolver`'s in parallel and returning the best scoring solution across all of the cores. Cythonized version of `make_move` is written in `life.pyx`, which is responsible for ~8x speedup in fitness scoring, and thus the overall performance.

## Credits

This implementation is based on Pavel Tyshevskyi's [repository](https://github.com/ptyshevs/rgol_ga) on the pre-2020 version of the CRGL competition. Thus, all the credits go to the team of that solution.
