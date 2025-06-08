## On the Effectiveness of Score-Based Diffusion Models for Data Augmentation: The Role of Sample Probability Density

자유전공학부 2021-19635 이선재

### 목차

- [연구 목적 및 개요](#연구-목적-및-개요)
- [논문재현](#논문-재현)
- [Results](#results)
- [Discussion](#discussion)
- [Conclusion](#conclusion)


### 연구 목적 및 개요

우선 위 프로젝트는 우선 아래의 논문을 기반으로 주제가 제안되었다.

> **Data Augmentation Using Diffusion Models to Enhance Inverse Ising Inference**, *Phys. Rev. E*, **111**, 045302 (2025).

해당 논문을 재현하고 논문의 결과를 발전시키고자 하는 방향에서 시작하였다. 논문은 다양한 상황에서 ising model을 inverse ising inference 할 때에 diffusion으로 증강된 데이터를 함께 넣는 것이 유리함을 증명한다. 본인은 위 프로젝트의 주제를 제안하며 위 논문이 굉장히 유용하다고 생각하였는데 가령 작년 굉장히 큰 이슈가 된 DeepSeek 과 같은 경우 chatgpt를 사용하여 학습을 한다. 점차 인공지능의 성능이 성장함에 따라 생성형 인공지능의 생성물을 학습물로써 활용하는 경우가 많아지는 시대에 이러한 방식으로 사람의 눈이 아닌 다른 방식으로 인공지능의 생성물이 유효한지 확인하는 것이 필요하다 생각하였다.
특히 위 논문의 경우는 ising model을 markov chain monte carlo process를 통해 데이터를 우선적으로 생성하고 해당 데이터를 바탕으로 diffusion을 학습하며 이로 생성된 데이터를 가지고 inverse ising inference의 성능을 향상시킨다. 여기에서 본인은 위와 같이 부족한 데이터를 diffusion 모델로 증강하여 사용하는 것이 가능하다는 논문의 주장에서 착안하여 왜 증강된 데이터가 성능을 좋게 할 수 있는지 파악하고자 하였다. 

### 논문 재현

