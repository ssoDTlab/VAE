# Variational Autoencoder (VAE) Study


## 📌 Introduction
Variational Autoencoder (VAE)는 확률적 생성 모델 중 하나로, 데이터의 잠재 표현(latent representation)을 학습하고 새로운 데이터를 생성할 수 있도록 설계된 신경망입니다.

이 저장소는 VAE에 대한 이론적 개념과 실습 내용을 정리하고, Google Colab에서 실험한 Jupyter Notebook 파일을 포함하고 있습니다.

## 📂 Repository Structure
```
📦 VAE-Study
 ┣ 📂 notebooks
 ┃ ┣ 📜 vae_basic.ipynb  # VAE 기본 개념 및 구현
 ┃ ┣ 📜 vae_mnist.ipynb  # MNIST 데이터셋을 활용한 VAE 실습
 ┃ ┣ 📜 vae_cifar10.ipynb # CIFAR-10 데이터셋을 활용한 VAE 실습
 ┣ 📜 README.md  # 프로젝트 개요 및 설명
 ┣ 📜 requirements.txt  # 필요 라이브러리 목록
```

## 🏗 Theory & Concepts
1. **Autoencoder (AE) vs. Variational Autoencoder (VAE)**
   - AE는 입력 데이터를 압축하고 복원하는 역할을 하지만, VAE는 확률적 분포를 학습하여 새로운 데이터를 생성할 수 있음.
   - VAE는 잠재 공간(latent space)에 정규 분포를 가정하고, KL Divergence를 이용해 이를 학습함.

2. **VAE Architecture**
   - Encoder: 입력 데이터를 잠재 변수의 확률 분포(평균, 분산)로 변환
   - Latent Space: 샘플링을 통해 새로운 데이터를 생성 가능
   - Decoder: 샘플링된 잠재 변수로부터 원본 데이터와 유사한 데이터를 생성

3. **Loss Function**
   - `Reconstruction Loss`: 원본 데이터와 복원된 데이터 간의 차이를 최소화
   - `KL Divergence Loss`: 잠재 분포가 정규 분포를 따르도록 유도

## 🛠 Installation & Usage
### 1️⃣ 환경 설정
필요한 라이브러리를 설치합니다.
```bash
pip install -r requirements.txt
```

### 2️⃣ Google Colab 실행
1. 이 저장소를 클론합니다.
   ```bash
   git clone https://github.com/your-username/VAE-Study.git
   ```
2. `notebooks/vae_basic.ipynb` 파일을 Colab에서 열고 실행합니다.

## 🏆 Results
### ✅ MNIST 데이터셋 결과 예시
| Input | Reconstructed |
|---|---|
| ![MNIST Input](https://upload.wikimedia.org/wikipedia/commons/2/27/MnistExamples.png) | ![Reconstructed](https://upload.wikimedia.org/wikipedia/commons/6/61/Autoencoder_mnist.png) |

## 🔗 References
- [Kingma & Welling, 2013 - Auto-Encoding Variational Bayes](https://arxiv.org/abs/1312.6114)
- [TensorFlow VAE Tutorial](https://www.tensorflow.org/tutorials/generative/cvae)
- [PyTorch VAE Example](https://github.com/pytorch/examples/tree/main/vae)

## 📜 License
MIT License
