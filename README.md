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
Or

```bash
conda env create -f environment.yml
conda activate ising-env
```

Make sure you are using Python 3.8 for reliable reproduce. And also since this code implements diffusion model and erasure machine, if you don't run this code with GPU it might take a long hour.
So make sure nvidia driver is installed.

# CODE

`/src/diffusion/finalcode.ipynb` : 최초 논문 재현을 위해 mcmc 방식을 활용해 제작된 샘플을 가지고 diffusion모델을 학습하는 코드입니다. 

`/src/diffusion/final_sample_*K.ipynb` : 앞선 finalcode.ipynb에서 생성한 diffusion을 불러오고 해당 모델에서 inverse ising inference 과정을 진행하여 plot하는 코드입니다. 총 3종류로 각각 finalcode.ipynb에서 학습한 epoch 이 1K, 10K, 32K 경우의 학습 모델을 가지고 추론을 진행하였습니다. 

---
`/src/cfg/g/ddpm_cfg.ipynb` : g의 값을 condition으로 넣고 condition free guidance를 구현한 결과로 해당 모델을 inverse ising inference 하는 결과 plot까지 포함하고 있습니다. 

`/src/cfg/energy/ddpm_cfg.ipynb` : 앞선 g 하위폴더의 ddpm_cfg와 동일하게 CFG를 활용하여 diffusion 모델을 실행하는 절차를 담고 있으나 energy 와 probability 기반으로 condition 을 주고 있으며 iii 결과 플롯은 아래의 다른 파일로 저장되어 있습니다. 

- `/src/cfg/energy/cfg_uncond_iii.ipynb` : energy 기반으로 생성된 condtional generation이 가능한 모델에서 unconditional 한 방식으로 데이터를 생성후 inverse ising inference 의 결과를 보여줍니다. 

- `/src/cfg/energy/cfg_cond_iii.ipynb` ; energy 기반으로 생성된 condtional generation이 가능한 모델에서 conditional 한 방식으로 데이터를 생성후 inverse ising inference 의 결과를 보여줍니다. 
# CONTACT

If you find any issues or have questions, feel free to [open an issue](https://github.com/satelite2517/ising-diffusion/issues) or contact us via email at [satelite2517@snu.ac.kr](mailto:satelite2517@snu.ac.kr).
