**"Sensorimotor Affordances in a Global Latent Workspace"**

---

### 초록 (Abstract)

인지에서 **구현체성(embodiment)**의 역할을 이해하는 것은 신경과학(neuroscience)과 인공지능(artificial intelligence) 양쪽 모두에서 발전을 이루기 위해 매우 중요하다. 생물학적 시스템은 의미를 부여하기 위해 다중감각 운동(sensory-motor) 상호작용에 의존하지만, 인공 모델은 이러한 기반(grounding)이 결여되어 있어 다양한 과제와 환경에서 일반화하는 능력이 제한된다.

본 연구에서는 **글로벌 잠재 워크스페이스(Global Latent Workspace, GLW)** 내에서 **감각운동 어포던스(sensorimotor affordances)**가 어떻게 발생하는지를 탐구한다. 우리는 **글로벌 워크스페이스 이론(Global Workspace Theory)**에서 영감을 받은 다중모달 딥러닝(multimodal deep learning) 아키텍처인 GLW를 설계하였으며, 이를 통해 시뮬레이션된 구현체 과제인 **Obstacle Tower Challenge**를 수행하는 **강화학습 에이전트(reinforcement learning agent)**를 훈련시킨다. 그리고 해당 에이전트의 감각-운동 데이터(sensory-motor data)를 활용하여, 각 모달리티(modality)에 연결된 **인코더-디코더 구조(encoder-decoder structure)** 기반의 GLW 다중모달 표현(multimodal representation)을 학습한다.

우리는 에이전트의 시점에서 획득한 이미지들의 GLW 표현을 **변분 오토인코더(variational autoencoder, VAE)** 기반 이미지 표현과 비교한다. 분석 결과, 감각운동 GLW는 시각 정보를 **구조화된 운동 잠재 공간(structured motor latent manifold)**으로 압축하며, 이는 어포던스와 관련된 표현들을 자연스럽게 군집화한다(clustering).

특히, 이러한 어포던스는 운동 상태(motor states)를 기반으로 **제로샷(zero-shot)** 방식의 시각 장면 생성을 가능하게 하며, 이는 **감각운동 이론(sensorimotor theories)**에 기반한 의식(consciousness) 연구에 대한 초기 실증적 근거를 제공한다. 어포던스를 공유된 잠재 공간(shared latent space)에 포함시킴으로써, GLW 프레임워크는 생물학적으로 영감을 받은 방식으로 보다 **일반화 가능하고 의미 기반(grounded)**인 인공知각(artificial perception)을 위한 경로를 제시한다.

---

**핵심 용어(Keywords)**:
구현된 인지(embodied cognition); 어포던스(affordance); 강화학습(reinforcement learning); 다중모달 학습(multimodal learning); 글로벌 워크스페이스 이론(global workspace theory); 감각운동 조건 이론(sensorimotor contingency theory); 의식(consciousness)

---

## 서론 (Introduction)

**감각운동 경험(sensorimotor experiences)**은 인간 지능(human intelligence)을 형성하는 데 있어 핵심적인 역할을 한다. 초기 발달 단계에서의 운동 활동(motor activity)은 공간적(spatial) 및 인과적 추론(causal reasoning)을 위한 신경 회로(neural circuits)를 조형한다 (Hadders-Algra, 2018). 하지만 현재의 인공지능(AI) 시스템은 주로 언어 통계(language statistics)에 기반하고 있어 시공간적(spatiotemporal) 관계를 이해하는 능력이 부족하다 (Bender & Koller, 2020; Huang et al., 2025).

시각-언어-행동 모델(vision-language-action models)이 이러한 문제를 해결할 가능성을 보여주고 있지만, 언어를 감각운동 능력(sensorimotor capabilities)과 완전히 통합하는 것은 여전히 도전 과제로 남아 있으며, 이는 **구현된 튜링 테스트(embodied Turing test)**와 같은 접근 방식에 대한 관심을 불러일으키고 있다 (Zador et al., 2023).

우리는 **글로벌 워크스페이스 이론(Global Workspace Theory, GWT)** (Baars, 1993; Mashour et al., 2020)과 **감각운동 조건 이론(Sensorimotor Contingency Theory)** (O’Regan & Noë, 2001; O’Regan, 2011)에 기반하여, 초기 형태의 의식(consciousness)은 실시간 감각운동 제어(real-time sensorimotor control)를 위해 진화했을 가능성이 있다고 제안한다.

최근 제안된 **글로벌 잠재 워크스페이스(Global Latent Workspace, GLW)** 프레임워크는 각각의 특화된 사전학습(pretrained) 모듈들을 인코더-디코더 쌍(encoder-decoder pairs)을 통해 통합한다 (Devillers et al., 2024; VanRullen & Kanai, 2021).

우리는 **Gibson의 어포던스 이론(affordances)** 및 구현된 에이전트(embodied agents)에 대한 선행 연구 (Clay et al., 2021, 2023; Gibson, 1979)를 바탕으로, 고성능 강화학습 에이전트로부터 수집한 자극-행동(stimulus-action) 쌍을 활용하여 **감각운동 GLW(Sensorimotor GLW)**를 훈련시킨다. 또한, 이 GLW를 **변분 오토인코더(Variational Autoencoder, VAE)**와 비교 분석함으로써, 현대 AI에 의식적 처리(conscious-like processing)를 통합하려는 초기 시도를 수행한다.

---

## 방법 (Methods)

### 데이터 수집 및 환경 (Data Collection and Environment)

감각운동 데이터(sensorimotor data)는 절차적으로 생성(procedurally generated)되는 3D 점프 앤 런 퍼즐 환경인 **Obstacle Tower Challenge**에서 훈련된 **강화학습 에이전트(reinforcement learning agent)**로부터 수집되었다 (Juliani et al., 2019).

에이전트는 크기 3×168×168의 **원시 이미지(raw images)**와 장면 및 환경에 대한 **메타정보(meta-information)**를 나타내는 11차원 벡터를 입력으로 받아들인다. 출력은 54차원의 **원-핫(one-hot)** 인코딩된 **행동 벡터(action vector)**이다.

총 **1,000만 스텝(10 million steps)** 동안 훈련을 수행한 후(일반적으로 에이전트가 레벨 4에 도달하는 시점), 우리는 **추론 실행(inference runs)**을 수행하여 총 **85만 쌍의 이미지-행동(image-action) 데이터**를 수집하였다.

최종적으로 학습된 강화학습 에이전트가 환경과 상호작용하는 영상을 아래 링크에서 확인할 수 있다:
[https://youtu.be/cNMItuHy\_J8](https://youtu.be/cNMItuHy_J8)

---

### 단일 모달 모듈 및 글로벌 잠재 워크스페이스(GLW) 학습

(Unimodal Modules and Global Latent Workspace (GLW) training)

**시각 모듈(vision module)**은 약 100,000차원의 이미지를 64차원의 **잠재 코드(latent code)**로 압축하기 위해 위에서 수집한 시각 데이터를 사용하여 **100 에폭(epochs)** 동안 훈련된 **변분 오토인코더(Variational Autoencoder, VAE)**를 활용하였다.

이에 반해, **운동 모듈(motor module)**은 별도의 학습이 필요 없다. 이 모듈은 54차원의 행동 출력을 **전진-후진(forward-backward), 좌우 이동(left-right), 점프(jumping), 회전(rotation)**을 나타내는 4개의 **이산 차원(discrete dimensions)**으로 인코딩한다.

이 두 모듈의 출력은 이후 **글로벌 잠재 워크스페이스(Global Latent Workspace, GLW)** 학습에 입력 데이터로 활용된다.

GLW는 두 모듈의 데이터를 하나의 **공유된 잠재 공간(shared latent space)**으로 통합하여 모달리티(modality) 간 정렬(alignment)을 보장하고, **입력 재구성(input retrieval)** 및 **교차 모달 변환(cross-modal translation)**, 혹은 **브로드캐스트(broadcast)**가 가능하게 한다.

GLW는 각 단일 모달 모듈(unimodal module)을 중심 워크스페이스에 연결하는 **3층 퍼셉트론(perceptron)** 기반의 **인코더-디코더 쌍(encoder-decoder pairs)**들로 구성된다. 구조는 그림 1(A)에 나타나 있다.

이 인코더-디코더 구조는 다음과 같은 손실 함수(losses)를 기반으로 최적화된다:

* **변환 손실(translation loss)**
* **대조 손실(contrastive loss)**
* **사이클 일관성 손실(cycle-consistency loss)**: 완전 사이클(full-cycle) 및 반 사이클(half-cycle)

(Devillers et al., 2024 참조)

우리는 GLW 아키텍처를 총 4종류 구현했으며, 각기 다른 층 크기(layer size)와 손실 가중치(loss weights)를 부여하여 **총 80만(image-action) 데이터 쌍에 대해 100 에폭(epoch)** 동안 학습시켰다.

이후의 분석에서는 가장 성능이 우수한 아키텍처 결과를 중심으로 설명하며, 이 아키텍처의 설정은 다음과 같다:

* 각 인코더/디코더 층당 뉴런 수: 96개
* 중앙 워크스페이스 크기: 32
* 모든 손실 항의 계수는 동일하되, **변환 손실(translation)**은 **2배로 증가**

기타 네트워크 설정을 사용하더라도 **정성적으로 유사한 결과(qualitatively similar results)**가 도출됨을 확인하였다.

---

## 결과 (Results)

### 어포던스 정확도 및 시각 재구성

(Affordance Accuracy and Visual Reconstruction)

**어포던스 정확도(affordance accuracy)**는 시각 모듈(vision module)을 입력으로 사용한 뒤, **GLW의 연속적인 운동 잠재 출력(GLW motor latent outputs)**을 기준으로, **강화학습 에이전트의 이산적 행동값(discrete RL action values)**과 비교하여 측정되었다. 결과는 그림 1(B)에 나타나 있다.

GLW 운동 잠재 벡터를 이산적 행동으로 변환할 때에는 **최근접 이웃 매핑(nearest neighbor mapping)**을 적용하였다. 예를 들어,

* 0.6은 1로,
* -0.3은 0으로,
* -0.7은 -1로
  매핑된다.

이러한 방식으로 **총 74%의 감각운동 어포던스 쌍(sensorimotor affordance pairings)**이 정확히 일치하는 것으로 나타났다.

**시각 재구성 손실(visual reconstruction loss)**은 원래의 **VAE 잠재 벡터(latents)**와, GLW 사이클을 한 번 완전하게 거친 후(vision → action → vision)의 잠재 벡터를 비교하여 **평균 제곱 오차(mean squared error, MSE)**로 측정되었다.

이 손실값은 **행동 유형(action category)**에 따라 달랐다. 예를 들어, 점프(jumping) 동작을 유도하는 드문 장면(rare event)은 더 높은 손실을 보였으며,

* 자주 나타나는 장면의 경우 MSE ≈ 0.4,
* 드문 경우에는 MSE ≈ 0.7에 달하였다.

---

### 감각운동 어포던스 클러스터

(Sensorimotor Affordance Clusters)

**잠재 표현(latent representations)**을 시각화하기 위해 **t-SNE(t-distributed Stochastic Neighbor Embedding)** 기법을 적용한 결과, GLW에서는 VAE보다 **더 뚜렷한 감각운동 어포던스 클러스터(sensorimotor affordance clusters)**가 형성되었다.

군집(clusters)은 다음 행동들에 대해 특히 분명하게 나타났다:

* **전진/후진(forward/backward)**
* **좌/우 이동(left/right slide)**
* **점프(jumping)**

반면, **회전(rotation)**에 대해서는 비교적 덜 뚜렷한 군집 형성을 보였다.

이러한 결과는 그림 1(B)의 **전진-후진 및 좌우 행동 차원에서의 첫 두 운동 잠재 차원(motor dimensions)** 시각화에 나타나 있다.

---

### 어포던스 장면 생성

(Affordance Scene Generation)

GLW의 **브로드캐스트 능력(broadcasting ability)**은 **운동 정보(motor information)**를 **시각 장면(visual scenes)**으로 직접 변환하는 기능을 가능하게 한다.

비록 원래의 **이산적 강화학습 행동 벡터(discrete RL motor outputs)**를 그대로 GLW 입력으로 디코딩하면 **다소 흐릿한 이미지(blurry images)**가 생성되지만, **4차원 운동 잠재 공간(motor latent space)**에서 **약간의 편차(slight deviations)**를 주면 **풍부하고 어포던스 특화된 장면(affordance-specific scenes)**이 생성된다.

예를 들어:

* **전진(forward)** 동작은 **깊은 시각 장면(deeper visual scenes)**을 만들어내며,
* **후진(backward)** 동작에서는 **벽(walls)**이 등장하였다.

이러한 잠재 공간 탐색(latent space traversal)을 시연한 영상은 다음 링크에서 확인할 수 있다:

* [전진 → 후진]: https://youtu.be/bsiUWs-81T0
* [우측 → 좌측 슬라이드]: https://youtu.be/ZAls1Ws5wzU

---

## 논의 및 전망 (Discussion and Outlook)

현대의 **다중모달 대규모 언어 모델(multimodal large language models, LLMs)**은 **강건한 공간 이해 능력(robust spatial understanding)**이 부족하며, 이는 구현체성(embodiment)을 필요로 할 수 있다 (Bender & Koller, 2020; Huang et al., 2025). 본 연구는 **글로벌 워크스페이스 이론(Global Workspace Theory, GWT)**과 **감각운동 조건 이론(Sensorimotor Contingency Theory)**을 **글로벌 잠재 워크스페이스(Global Latent Workspace, GLW)**라는 수학적으로 다룰 수 있는 모델로 통합하며, **구현된 지능(embodied intelligence)**과 그것이 **의식 유사 정보 처리(conscious-like information processing)**와 어떤 관련이 있는지를 보다 심층적으로 이해할 수 있는 기반을 제공한다.

그럼에도 불구하고, 우리가 제안한 GLW는 여전히 단순한 **인코더-디코더 구조(encoder-decoder structure)**에 불과하며, 완전하게 통합된 에이전트(fully integrated agent)는 아니다. 이 간극을 메우기 위해 **강화학습(RL)**과 **GLW 학습(GLW training)**을 결합하는 것은 **최첨단 구현형 로봇 시스템(state-of-the-art embodied robotic systems)**을 실현하고, **구현된 튜링 테스트(embodied Turing test)**에 접근하기 위한 유망한 방향이 될 수 있다 (Zador et al., 2023).

또한, 우리의 생성 결과(generative results)는 **예측 처리(predictive processing)**를 **운동 어포던스(motor affordances)**와 통합할 경우, 보다 **강건하고 잡음에 강한 표현(noise-resistant representations)**을 만들 수 있음을 시사한다 (Seth, 2014; Taniguchi et al., 2023).

향후 연구는 GLW가 생성한 어포던스를 활용한 **후속 시각 과제(downstream visual tasks)** 성능을 평가하는 데 집중할 예정이다. 예를 들어, **장애물까지의 거리(distance to obstacles)**를 예측하는 과제 등에서 그 실용적 유용성을 검증하려 한다.

초기 결과는 GLW 표현이 기존의 **변분 오토인코더(Variational Autoencoder, VAE)**보다 **공간 관계(spatial relationships)**를 더 효과적으로 인코딩함을 시사하며, 이는 **구현된 지능(embodied intelligence)**이 가지는 인지적 이점(cognitive benefits)을 더 깊이 탐구할 수 있는 가능성을 연다.

---

## 그림 1 설명 (Figure 1)

**A**
**변분 오토인코더(Variational Autoencoder, VAE)**는 **강화학습 에이전트(reinforcement learning agent)**가 추론(inference) 실행 중에 수집한 이미지들을 재구성하기 위해 학습된다.
VAE로부터 추출된 **잠재 벡터(latent vectors)**는 **시각 모듈(vision module)**로 사용되며, **운동 모듈(motor module)**의 출력과 함께 **단일 모달 입력(unimodal inputs)**으로 활용되어 **글로벌 잠재 워크스페이스(Global Latent Workspace, GLW)**에 입력된다.

시각 인코더 **eV(encoder for vision)**와 운동 인코더 **eM(encoder for motor)**는 이 입력을 **공유된 잠재 표현(shared latent representation)**인 GLW로 사상(mapping)한다.
시각 디코더 **dV(decoder for vision)**와 운동 디코더 **dM(decoder for motor)**는 GLW 표현을 각 단일 모달 도메인(unimodal domain)의 형식으로 다시 변환하며, 이로써 **글로벌 워크스페이스 이론(Global Workspace Theory, GWT)**의 핵심 개념인 **“브로드캐스트(broadcast)”**가 구현된다.

---

**B**
GLW의 운동 디코더 **dM**가 출력한 **전진-후진(forward-backward)** 및 **좌우 이동(left-right)** 행동 차원에 대한 운동 분포(motor distribution).
각 운동 잠재 벡터(motor latent vector)는 **이산적 강화학습 행동값(discrete RL ground-truth values)**에 따라 색깔로 구분되었다.

예를 들어,

* **녹색(green)**은 입력 이미지 장면이 강화학습 에이전트에 의해 **전진 행동값 1**로 매핑된 경우의 운동 잠재 출력값을 의미한다.

아래의 **GLW t-SNE 임베딩(GLW t-SNE embeddings)**은 GLW 중앙 층(central layer)에서의 잠재 표현(latent representations)을 시각화한 것이며, 색상 코딩은 위의 운동 분포와 동일하다.
비교를 위해 **VAE의 t-SNE 시각화(VAE t-SNE)**도 함께 제공되었다.

---