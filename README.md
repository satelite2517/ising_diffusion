# ISING DIFFUSION

This repository contains the final project code for Team 3 in the course ***계산, 학습, 그리고 물리 / Computation, Learning, and Physics (M1419.002300)*** at Seoul National University (SNU). Completed during Spring 25 by Heejae Shin, Minho Ahn (Physics & Astronomy), and Yudam Son, Seonjae Lee (Liberal Studies), SNU.

This work is originally based on:

> **Data Augmentation Using Diffusion Models to Enhance Inverse Ising Inference**, *Phys. Rev. E*, **111**, 045302 (2025).

We reproduce and extend the results presented in this paper as part of our final project.


```

ising-diffusion/
├── figure/         # Generated plots and visualizations
├── src/            # Source code
│   ├── diffusion/
|   ├── cfg/ 
│   └── function  
├── report/         # Final presentation slides and project report
├── data/           # Input data and sample datasets
├── requirements.txt
└── README.md

```
If you want to see how the function is structured, then check out `src/fucntion/`.
Else if you want to reproduce the figure or check out it runs properly check out each folders in `src/`. Also we add some source files that does not produce the figure in the presentation file. These are the source files contain some results that was helpful during the project and discussed at final report. 

# INSTALLATION

Clone the repository and install the required dependencies:

```bash
git clone https://github.com/satelite2517/ising-diffusion.git
cd ising-diffusion
pip install -r requirements.txt
```

Make sure you are using Python 3.8 for reliable reproduce. And also since this code implements diffusion model and erasure machine, if you don't run this code with GPU it might take a long hour.
So make sure nvidia driver is installed.

# CONTACT

If you find any issues or have questions, feel free to [open an issue](https://github.com/satelite2517/ising-diffusion/issues) or contact us via email at [satelite2517@snu.ac.kr](mailto:satelite2517@snu.ac.kr).
