# Numerical experiments for "Fluctuations of sample eigenvalues in a spiked covariance model with Haar-rotated spikes: a transition at $p^2 \asymp n$"

Code for the numerical experiments of Noriyoshi Sakuma and Jean-Lou Valeau, "Fluctuations of sample eigenvalues in a spiked covariance model with Haar-rotated spikes: a transition at $p^2 \asymp n$".

The paper studies the eigenvalues of a sample covariance matrix when the population covariance has randomly rotated spikes. The notebook simulates this model, in the real and in the complex case, and compares the simulated eigenvalues with the limit laws of the paper.

## Contents

- `spiked_haar_experiments_v2.ipynb`: the code, with its output (the figures).
- `requirements.txt`: Python packages.
- `LICENSE`

No external data is used. Everything is simulated.

## Experiments

We use the notation of the paper: $p$ is the dimension, $n$ is the number of samples, $r = s = 1$, $\alpha_1 = 10, \beta_1 = 5$ and $\sigma^2 = 1$. We follow the largest spike, $\theta = 10$.

1. Histograms of the fluctuation of the largest sample eigenvalue at the scale $\sqrt n$, in the real and in the complex case. There are four pairs $(p, n)$, one for each regime of the paper: (2500, 2500), (500, 5000), (500, 50000) and (100, 50000). The histograms are compared with the law predicted by the paper.
2. The same histograms at the scale $p$.
3. Wasserstein distance between the normalised fluctuation and three laws: $W_\ell$ alone (the Haar term), the Gaussian term alone, and their sum. The distance is plotted against $p^2/n$, with $n = 20000$ and $p$ from 10 to 1500 (real case only).

## Usage

Python 3.13 was used to produce the figures. Install the packages and open the notebook:

```
pip install -r requirements.txt
jupyter notebook spiked_haar_experiments_v2.ipynb
```

Then run all the cells from top to bottom.

## Reproducibility

All random generators are seeded (`SEED = 42` in the notebook). A new run should give the same figures, up to small numerical differences between machines.

## License

MIT. See `LICENSE`.
