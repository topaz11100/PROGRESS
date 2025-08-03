**"A foundation model to predict and capture human cognition"**
---

### 초록 (Abstract)

통합된 인지 이론(cognition theory)을 정립하는 것은 심리학(psychology)에서 오랫동안 중요한 목표였다.
이러한 이론을 향한 첫걸음은 **다양한 상황에서 인간 행동(human behaviour)**을 예측할 수 있는 **계산 모델(computational model)**을 만드는 것이다.
본 논문에서는 자연어(natural language)로 표현 가능한 어떤 실험에서도 **인간 행동을 예측하고 시뮬레이션**할 수 있는 계산 모델인 **Centaur**를 소개한다.

Centaur는 최첨단 언어 모델(state-of-the-art language model)을 대규모 데이터셋 **Psych-101**에 대해 **파인튜닝(fine-tuning)**하여 개발되었다.
Psych-101은 **160개의 실험에서 수행된 1,000만 회 이상의 선택(choice)**과 **60,000명 이상의 참가자**로부터 얻은 **trial-by-trial 데이터**를 포함하는, 전례 없는 규모의 데이터셋이다.

Centaur는 기존의 인지 모델(cognitive models)보다 **검증 대상 참가자(held-out participants)**의 행동을 더 잘 포착(capture)할 뿐 아니라,
**이전에 본 적 없는 시나리오(cover stories)**, **과제 구조(task structure)의 수정**, **완전히 새로운 도메인**에도 일반화(generalize)된다.
게다가 파인튜닝 이후 모델의 **내부 표현(internal representations)**은 **인간의 뇌 활동(neural activity)**과 더 밀접하게 정렬(aligned)된다.

이러한 결과들을 종합하면, **넓은 범위의 도메인에서 인간 행동을 포착할 수 있는 계산 모델을 발견하는 것이 가능함**을 보여준다.
우리는 이러한 모델들이 인지 이론(cognitive theories) 개발을 안내하는 데 **엄청난 잠재력(tremendous potential)**을 가지고 있다고 믿으며,
이 가능성을 보여주는 **사례 연구(case study)**를 함께 제시한다.

---

인간의 정신(human mind)은 놀라울 정도로 **범용적(general)**이다\[^3].
우리는 아침에 어떤 시리얼을 먹을지, 어떤 옷을 입을지와 같은 **일상적인 결정(mundane decisions)**을 내릴 뿐 아니라,
**암 치료 방법을 찾거나 우주를 탐사하는 것과 같은 복잡한 문제(complex challenges)**에도 도전한다.
우리는 몇 번의 시연(demonstrations)만으로 **기술(skill)**을 습득하고\[^4],
**인과적으로(reason causally)** 사고하며\[^5], **호기심(curiosity)**을 통해 행동에 동기를 부여받는다\[^6].
산을 오르든, 비디오 게임을 하든, 예술 작품을 창조하든,
이러한 **다재다능함(versatility)**은 인간됨의 본질을 정의한다.

---

반면, 대부분의 현대 계산 모델(contemporary computational models)은 **도메인 특화(domain specific)**되어 있다.
이들은 특정한 한 문제에서만 뛰어난 성능을 보이도록 설계되었으며, 그 **문제 이외의 것에는 적용되지 않는다**.
예를 들어 보자. **AlphaGo**는 바둑 게임(Go)을 마스터하기 위해 **구글 딥마인드(Google DeepMind)**에서 개발된 컴퓨터 시스템이다\[^7].
이 시스템은 해당 게임에서는 인상적인 수준으로 플레이할 수 있지만, 그 외의 일은 거의 할 수 없다.

인지과학(cognitive sciences)에서도 이와 유사한 양상이 관찰된다.
예를 들어, **전망 이론(prospect theory)**은 인간 인지(human cognition)에 관한 가장 영향력 있는 설명 중 하나로,
사람들이 어떻게 선택을 하는지를 이해하는 데 있어 귀중한 통찰을 제공한다\[^8].
그러나 이 이론은 사람들이 **어떻게 학습(learn)**하고, **계획(plan)**하며, **탐색(explore)**하는지에 대해서는 아무것도 알려주지 않는다.

---

만약 우리가 인간의 정신(human mind)을 **전체적으로(entirely)** 이해하고자 한다면,
**도메인 특화 이론(domain-specific theories)**에서 **통합된 이론(an integrated theory)**으로 나아가야만 한다.
이러한 통합적 접근(unified approach)의 중요성은 이미 우리 분야의 선구자들(pioneers)에 의해 인식되어 왔다.
예를 들어, 1990년에 다음과 같은 말이 있었다.

> “통합된 인지 이론(unified theories of cognition)만이
> \[우리의] 놀랍도록 증가하고 있는 지식 자산(fund of knowledge)을
> 지적 통제(intellectual control) 하에 둘 수 있는 유일한 방법이다.”\[^2]

그렇다면 우리는 어떻게 이러한 이론을 향해 **의미 있는 진전(meaningful progress)**을 이룰 수 있을까?

---

통합된 인지 이론(unified theory of cognition)을 향한 중요한 단계는,
**어떤 도메인(domain)**에서도 **인간 행동(human behaviour)을 예측하고 시뮬레이션(simulate)**할 수 있는 **계산 모델(computational model)**을 구축하는 것이다\[^2,^9].
이 논문에서 우리는 이러한 도전을 받아들여,
**Centaur**라는 **기초 모델(foundation model)**을 소개한다.
Centaur는 **인간 인지(human cognition)**에 대한 기초 모델로서,
**대규모 인간 행동 데이터(corpus of human behaviour)**에 대해
**최첨단 대형 언어 모델(state-of-the-art large language model)**을 **데이터 기반 방식(data-driven manner)**으로 파인튜닝(fine-tuning)하여 설계되었다.

이를 위해 우리는 **Psych-101**이라는 **대규모 데이터셋(large-scale dataset)**을 구성하였다.
이 데이터셋은 **160개의 심리학 실험(psychological experiments)**에서의 trial-by-trial 데이터를 포함하고 있다
(자세한 사항은 Methods의 ‘Data collection’ 및 Extended Data Fig. 1 참조).
우리는 각 실험을 **자연어(natural language)**로 전사(transcribe)하였으며,
이를 통해 매우 다양한 실험 패러다임(experimental paradigms)을 **공통된 형식(common format)**으로 표현할 수 있었다\[^12,^13].

---

그 결과로 생성된 데이터셋은 전례 없는 규모를 자랑하며,
1,000만 개 이상의 인간 선택(human choices)을 포함하고 있고,
다중 슬롯머신 문제(multi-armed bandits), 의사결정(decision-making), 기억(memory),
지도 학습(supervised learning), 마르코프 결정 과정(Markov decision processes) 등과 같은
다양한 도메인의 **대표적 연구들(canonical studies)**을 포괄하고 있다
(개요 및 예시는 Fig. 1a 참조).

우리는 Centaur를 다양한 **엄밀한 테스트(rigorous tests)**에 적용하였으며,
그 결과 Centaur가 여러 수준의 일반화(generalization)에서 **인간 행동(human behaviour)**을
정확하게 포착한다는 것을 입증하였다.
먼저, Centaur는 **학습 데이터에 포함되지 않은 참가자(held-out participants)**의 행동을
기존 인지 모델(cognitive models)보다 더 정확하게 예측함을 보였다.
다음으로, Centaur는 **학습되지 않은 실험(held-out experiments)**에 대해서도
그 예측 능력을 일반화할 수 있음이 나타났다.
이 맥락에서 우리는 Centaur가 **수정된 시나리오(cover stories)**,
**문제 구조(problem structures)**,
심지어 **완전히 새로운 도메인(entirely new domains)**에서도
정확하게 인간 행동을 예측함을 발견하였다.
마지막으로, **Centaur의 내부 표현(internal representations)**은
명시적으로 **인간의 신경 활동(neural activity)**을 학습 대상으로 삼지 않았음에도 불구하고
더욱 **인간 정렬(human-aligned)**되었다는 것을 확인하였다.

---

이 모든 결과를 종합하면,
**광범위한 도메인에 걸쳐 인간 행동(human behaviour)을 포착할 수 있는 계산 모델(computational model)**을
발견하는 것이 가능하다는 사실이 입증된다.
우리는 이러한 **예측 모델(predictive model)**이 **인간 정신(human mind)**을
더 잘 이해하는 데 있어 **많은 직접적인 기회(direct opportunities)**를 제공한다고 믿는다\[^14,^15].
그리고 이러한 가능성을 보여주기 위해 **사례 연구(case study)**를 제시한다.

---

### 모델 개요 (Model overview)

우리는 Centaur를 **오픈소스 언어 모델(open-source language model)**인
**Llama 3.1 70B** 위에 구축하였다.
이는 Meta AI가 사전 학습(pretraining)한 **최첨단 모델(state-of-the-art model)**이며
이하에서는 이 모델을 간단히 **Llama**라고 부른다\[^11].

이처럼 대형 언어 모델(large language model)을 **백본(backbone)**으로 사용하는 것은
이러한 모델에 내재된 **방대한 지식(knowledge)**을 활용할 수 있게 해주었다.
Centaur의 학습 과정은 **Psych-101** 데이터셋에 대해
**QLoRA(Quantized Low-Rank Adaptation)**라고 불리는
**파라미터 효율적 파인튜닝(parameter-efficient fine-tuning)** 기법을 활용하여 이루어졌다\[^16].

QLoRA는 **4비트 양자화된 언어 모델(quantized language model)**을
**고정(frozen)**된 **기반 모델(base model)**로 사용하고,
여기에 **저차원 어댑터(low-rank adapters)**를 추가하는 방식이다.
기반 모델의 파라미터는 변경되지 않으며,
소수의 **추가 가능한 파라미터(trainable parameters)**만이
어댑터에 포함된다.
이들은 일반적으로 **하프 프리시전 부동소수점 형식(half-precision floating-point format)**으로 표현된다.

우리의 경우, 우리는 모든 **비임베딩 계층(non-embedding layers)**
— 즉, 자기 주의(self-attention) 메커니즘과 피드포워드 네트워크의
모든 선형 계층(linear layers) — 에 대해
**랭크(rank) r = 8**인 저차원 어댑터를 추가하였다
(Fig. 1b 참조).

이 설정에서는 새로 추가된 파라미터들이
전체 기반 모델 파라미터의 **0.15%** 수준이다.
우리는 전체 데이터셋에 대해 **한 에폭(epoch)** 동안
**표준 크로스 엔트로피 손실(standard cross-entropy loss)**을 사용하여 모델을 학습하였다.
이때 **인간 응답(human responses)**에 해당하지 않는 토큰은
손실 계산에서 **마스킹(masked out)**하여,
모델이 실험 지침을 완성하는 것이 아니라
**인간 행동을 포착하는 데 집중**하도록 하였다.

전체 학습 과정은 **A100 80GB GPU**에서 약 **5일**간 소요되었다
(Methods, ‘Fine-tuning procedure’ 참조).

---

### Centaur는 인간 행동을 포착한다 (Centaur captures human behaviour)

우리는 Centaur가 **인간 행동(human behaviour)**을 **견고하게(robustly)** 포착한다는 것을 입증하기 위해,
여러 종류의 **제외 데이터(held-out data)**에 대해 Centaur를 평가하였다.

첫 번째 분석에서는,
**학습 데이터에 포함되지 않은 참가자(participants)**의 행동을
Centaur가 예측할 수 있는지를 테스트하였다.
이를 위해 각 전사된 실험(transcribed experiment)을 두 부분으로 나누었고,
전체 참가자의 **90%는 학습(training)**에 사용하고
**10%는 테스트(testing)**에 보존하였다.

우리는 인간 응답에 대한 **적합도(goodness-of-fit)**를
응답 전체에 대해 평균을 낸 **음의 로그 우도(negative log-likelihood)**로 측정하였다
(Methods, ‘Evaluation metric’ 참조).
이 분석 결과는 Fig. 2a에 제시되어 있으며,
Centaur를 파인튜닝하지 않은 기반 모델(base model)과
인지과학 문헌에서 **최신 상태(state-of-the-art)**로 간주되는
여러 **도메인 특화 모델(domain-specific models)**들과 비교하였다
(Extended Data Table 1 참조).

실험들 간에 예측력에는 상당한 분산이 있었으나
(Centaur 평균: 0.49; Llama 평균: 0.47),
**파인튜닝은 항상 적합도를 향상**시켰다.
파인튜닝 이후, 전체 실험에 걸친 평균 로그우도 차이는 **0.14**였다
(Centaur 음의 로그우도: 0.44; Llama 음의 로그우도: 0.58;
단측 t-검정: t(1,985,732) = –144.22, P ≤ 0.0001; Cohen’s d = 0.20).

---

더불어 우리는 Centaur를 앞서 언급한
여러 **도메인 특화 인지 모델(domain-specific cognitive models)**들과 비교하였다.
이들 모델에는 **일반화 맥락 모델(generalized context model)**\[^17],
**전망 이론 모델(prospect theory model)**\[^18],
그리고 다양한 **강화 학습 모델들(reinforcement learning models)**\[^19,^20]이 포함된다
(Methods, ‘Domain-specific cognitive models’ 참조).

그 결과, Centaur는 **모든 실험 중 단 하나를 제외하고는**,
이러한 도메인 특화 인지 모델들보다
**더 높은 인간 행동 예측 성능(predictive performance)**을 보였다.

Centaur와 도메인 특화 모델들 간의 평균 음의 로그우도 차이는 **0.13**이었다
(인지 모델의 음의 로그우도: 0.56;
단측 t-검정: t(1,985,732) = –127.58, P ≤ 0.0001; Cohen’s d = 0.18).

Extended Data Fig. 2와 3에는
**비행동 데이터(non-behavioural data)**로 파인튜닝된 모델들과의 비교,
그리고 **노이즈 천장 분석(noise-ceiling analysis)**가 추가로 제시되어 있다.

---

이전 분석들은,
**이전에 수행된 행동(previously executed behaviour)**을 조건으로 한
인간 응답(human responses)의 예측에 초점을 맞추었다.
하지만 우리는 다음과 같은 질문을 던질 수 있다:

> Centaur가 **열린 루프 방식(open-loop fashion)** — 즉,
> **자신의 응답을 다시 입력으로 사용하는 방식** — 으로
> **인간 유사 행동(human-like behaviour)**을 생성할 수 있는가?

이러한 설정은 **모델의 능력을 더욱 강하게 시험하는 방식**으로 간주되며,
때때로 **모델 반증(model falsification)**이라고도 불린다\[^21].

Centaur가 이 검증을 통과하는지 확인하기 위해,
우리는 서로 다른 세 가지 실험 패러다임에서 **열린 루프 시뮬레이션(open-loop simulations)**을 수행하고,
이 시뮬레이션에서 얻어진 통계 분포(statistics distributions)를 분석하였다.

우선, 우리는 Centaur를 **horizon-task 패러다임**에 대해 시뮬레이션하였다.
이 과제는 **2개의 슬롯머신(two-armed bandit)** 중에서 반복적으로 선택하는 형태이며,
**탐색 전략(exploration strategies)**의 유형을 감지하기 위해 사용된다\[^20].
그 결과, Centaur는 **평균 54.12, 표준편차 2.89**의 성능을 보였으며,
이는 인간 참가자의 평균 성능 **52.78, 표준편차 2.90**과 유사하였다.
이 유사성은 **±3 포인트 허용 범위**를 가진
**쌍방향 단측 t-검정(two one-sided t-tests procedure)**를 통해 통계적으로 검증되었으며
**P = 0.02**로 나타났다.

Centaur는 또한 **불확실성 기반의 지향 탐색(uncertainty-guided directed exploration)**에서도
인간과 유사한 수준의 행동을 보였다 (Fig. 2b).
이는 많은 현대 언어 모델들에서 **명확하게 결여되어 있는 패턴**이다\[^12].

---

우리는 또한 Centaur가 단순히 **평균 참가자(average participant)**의 행동만 포착하는 것이 아니라,
**전체 집단(population)**이 생성하는 **행동 경로의 분포(distribution over trajectories)** 자체를
모사한다는 것을 관찰하였다.

예를 들어, **two-step task**는
**모델 기반(model-based)**과 **모델 자유(model-free)** 강화 학습(reinforcement learning)을 구분하기 위해 자주 사용되는
잘 알려진 실험 패러다임이다\[^19].
이 과제에서 Centaur는 인간 피험자들처럼
다음과 같은 다양한 학습 경로를 생성하였다:

* **순수하게 모델 자유(model-free)**적인 학습 경로
* **순수하게 모델 기반(model-based)**적인 학습 경로
* **그 혼합(mixture)**된 형태의 경로들

이러한 경로들은 Fig. 2c에 제시된 **이중봉 분포(bimodal distribution)**로 표현된다.

---

마지막으로, 우리는 Centaur가 **비인간 행동(non-human behaviour)**을 예측하는 데 실패하는지를 검증하였다.
이를 위해 우리는 참가자들에게 **4개의 대표적인 경제 게임(canonical economic games)**에서
**인간의 응답** 또는 **인공 에이전트(artificial agent)**의 응답을 예측하도록 요구한 기존 연구를 활용하였다\[^22].

Centaur 역시, 원래의 인간 실험 결과를 반영하여,
**인간의 응답(human responses)**은 정확히 예측하였으나
**인공 에이전트의 응답(artificial responses)**은 예측에 어려움을 겪었다
(Fig. 2d 참조).

* 인간 응답 예측 정확도: **64%**
* 인공 에이전트 응답 예측 정확도: **35%**
* 단측 t-검정: t(230) = 20.32, P ≤ 0.0001

이러한 결과들은, Centaur가 다양한 상황에서
**인간 유사 특성(human-like characteristics)**을 보이며,
**의미 있는 열린 루프 행동(open-loop behaviour)**을 생성할 수 있음을 시사한다.

---

### 일반화 능력 탐색 (Probing generalization abilities)

지금까지 우리는 Centaur가
**학습에 사용된 실험(training experiments)** 내에서
**새로운 참가자(previously unseen participants)**에 대해서도 일반화(generalize)할 수 있음을 보여주었다.

그러나 **진정한 인간 인지의 기초 모델(true foundation model of human cognition)**이라면
**학습에 포함되지 않은 임의의 실험(arbitrary experiment)**에서도
**인간 행동(human behaviour)**을 포착할 수 있어야 한다.

이를 검증하기 위해, 우리는 Centaur를
점차 더 복잡한 **분포 외 평가(out-of-distribution evaluations)** 시리즈에 노출시켰다.

---

먼저, 우리는 Centaur가 **겉표현(cover story)**의 변화에 대해 견고한지를 조사하였다.
이 분석에서는 참고문헌 \[23]에 수록된 데이터를 활용하였다.
해당 연구는 앞서 언급된 **two-step task**를 사용하였으며,
기존의 **기본 이야기(canonical cover story)**인
"외계 행성을 여행하는 우주선(spaceships traveling to foreign planets)" 설정 외에,
**마법 양탄자(magical carpets)**에 관한 **새로운 커버 스토리(new cover story)**를 도입하였다.

중요한 점은, **Psych-101**은
우주선 커버 스토리를 사용하는 실험은 포함하지만\[^24],
마법 양탄자 커버 스토리를 포함하는 실험은 전혀 포함하지 않는다.

그럼에도 불구하고, 우리는 Centaur가
참고문헌 \[23]에 수록된 **마법 양탄자 실험(magic-carpet experiment)**에서의
**인간 행동을 정확하게 포착(capture)**한다는 것을 발견하였다 (Fig. 3a 참조).

앞선 분석과 마찬가지로,
**파인튜닝(fine-tuning)** 후의 성능 향상이 관찰되었고,
도메인 특화 인지 모델(domain-specific cognitive model)과 비교하였을 때도
**우수한 적합도(goodness-of-fit)**를 보였다.

* Centaur 음의 로그우도: 0.51
* Llama 음의 로그우도: 0.63
* 인지 모델 음의 로그우도: 0.61
* Centaur vs Llama 단측 t-검정: t(9,701) = –24.7, P ≤ 0.0001
* Centaur vs 인지 모델 단측 t-검정: t(9,701) = –20.7, P ≤ 0.0001

이때 사용된 인지 모델은
**모델 기반(model-based)** 및 **모델 자유(model-free)** 강화학습을 결합한 **하이브리드 모델(hybrid model)**이다\[^19].

---

두 번째 **분포 외 평가(out-of-distribution evaluation)**로,
우리는 Centaur가 **과제 구조(task structure)**의 변화에 대해
견고한지를 실험하였다.

이를 위해 우리는 **Maggie’s farm**이라는 패러다임에 Centaur를 노출시켰다\[^25].
Maggie’s farm은 앞서 언급한 **horizon task**의 확장 버전으로,
선택지로 **세 개의 옵션(third option)**이 추가된다.

Psych-101에는 여러 **two-armed bandit (2개 선택지 슬롯머신)** 실험이 포함되어 있으며
그 안에는 horizon task도 있다.
하지만 Maggie’s farm이나 그 외의 **three-armed bandit (3개 선택지 슬롯머신)** 실험은 포함되어 있지 않다.

따라서 이 분석은 Centaur가
**과제 구조의 변경(structural task modifications)**에 대해
얼마나 견고한지를 검증하는 실험이다.

우리는 Centaur가 Maggie’s farm에서도
**인간 행동(human behaviour)**을 정확히 포착한다는 것을 발견하였다 (Fig. 3b 참조).

이번에도 다음과 같은 결과가 나타났다:

* 파인튜닝 후 성능 향상(fine-tuning benefit)
* 도메인 특화 인지 모델과 비교했을 때 **우수한 적합도(goodness-of-fit)**
* 도메인 특화 모델은 해당 설정에 **잘 일반화하지 못함**

음의 로그우도(negative log-likelihood) 결과는 다음과 같다:

* Centaur: 0.42
* Llama: 0.62
* 인지 모델: 0.98
* Centaur vs Llama 단측 t-검정: t(510,153) = –204.2, P ≤ 0.0001
* Centaur vs 인지 모델 단측 t-검정: t(510,153) = –559.8, P ≤ 0.0001

---

마지막으로, 우리는 Centaur가 **완전히 새로운 도메인(entirely new domains)**에서도
**인간 행동(human behaviour)**을 포착할 수 있는지를 조사하였다.

이 분석에서는 **논리적 추론(logical reasoning)**을 다루는 연구를 고려하였다\[^26].
Psych-101에는 **확률적(probabilistic)** 및 **인과적 추론(causal reasoning)** 문제는 포함되어 있지만,
우리는 의도적으로 **논리적 추론(logical reasoning)**을 포함하는 연구는 모두 제외하였다.

앞선 분석들과 마찬가지로, 이 경우에도
**파인튜닝(fine-tuning)**은 긍정적인 효과를 나타냈다:

* Centaur 음의 로그우도: **1.65**
* Llama 음의 로그우도: **1.92**
* 단측 t-검정: t(198,406) = –50.39, P ≤ 0.0001
* Cohen’s d = 0.23

이 설정에서는 도메인 특화 인지 모델(domain-specific cognitive model)과의 비교는 수행하지 않았다.
왜냐하면, 학습 데이터에 관련된 문제 유형이 전혀 포함되어 있지 않아,
**의미 있는 전이(transfer)**를 수행할 수 있는 모델을 구성하기가 어렵기 때문이다.

---

우리는 이러한 결과들을 보강하기 위해,
**학습 데이터에 어떤 형태로도 포함되지 않은**
6개의 추가적인 **분포 외 실험 패러다임(out-of-distribution experimental paradigms)**에서
Centaur를 분석하였다.

이 실험들에는 다음이 포함된다:

* **도덕적 의사결정(moral decision-making)**\[^27]
* **경제 게임(economic games)**\[^28]
* **자연적 범주 및 보상 학습(naturalistic category and reward learning)**\[^29]
* **행동 경향(behavioural propensities)**\[^30]
* **심층 순차 의사결정 과제(deep sequential decision task)**\[^31]

이 분석들에서 Centaur는
**모든 설정에서 인간 행동을 견고하게 포착(robustly captured human behaviour)**하였다.
반면, **더 작은 모델(smaller models)**이나
**파인튜닝되지 않은 모델(non-fine-tuned models)**은
일관되게 그 수준을 달성하지 못하였다
(Extended Data Fig. 4 참조).

---

우리는 인간의 **선택 데이터(human choice data)**를 분석하는 것 외에도,
Centaur가 **인간 반응 시간(human response times)**을 예측할 수 있는지도 조사하였다.

**Hick의 법칙(Hick’s law)**\[^32]에 따르면,
개인의 반응 시간은 **반응 엔트로피(response entropy)**의 **선형 함수(linear function)**이다.
이에 따라, 우리는 Psych-101에 포함된 일부 실험에서
약 **400만 개**의 반응 시간 데이터를 추출하였다.

그 후, 우리는 서로 다른 계산 모델에서 유도된 반응 엔트로피를 기반으로
**로그 변환된 반응 시간(log-transformed response times)**을 예측하기 위한
**세 가지 선형 혼합 효과 모델(linear mixed effects models)**을 적합시켰다.

그 결과, Centaur에서 유도된 반응 엔트로피가
반응 시간의 분산을 가장 잘 설명하였다:

* Centaur의 조건부 결정계수 (conditional R²): **0.87**
* Llama의 조건부 결정계수: **0.75**
    → 로그 베이지안 인자(log Bayes factor): log \[BF₍Centaur, Llama₎] = 53,773.5
* 도메인 특화 인지 모델의 조건부 결정계수: **0.77**
    → log \[BF₍Centaur, cognitive models₎] = 14,995.5

이 결과는 Centaur가 **단순한 선택 데이터 이상으로 확장되는 예측 능력**을 가지고 있음을 보여준다.

---

모델이 사전 학습(pretraining)된 문제들에서
**성능이 저하되지 않았는지(degradation)**를 확인하기 위해,
우리는 Centaur를 **머신러닝 문헌(machine-learning literature)**에서
제안된 여러 벤치마크에서 검증하였다\[^33,^34].

그 결과 Centaur는
**성능 기반 벤치마크(performance-based benchmarks)**에서 안정적인 성능을 유지하였으며,
일부 벤치마크에서는 **기반 모델(base model)**보다
오히려 더 나은 성능을 보이기도 하였다
(Extended Data Fig. 5a, 5b 참조).

마지막으로, **인간 정렬(human alignment)**을 측정하는 벤치마크들에서는
Centaur의 내부 표현이
**더 인간적인 특성(human-like characteristics)**으로
**변화**한 것을 관찰하였다 (Extended Data Fig. 5c 참조).

Fig. 4a는 이러한 정렬의 개선을 시각적으로 보여주며,
이는 **CogBench**라고 불리는 벤치마크에서
10개의 인지 지표(behavioural metrics)를 기반으로 파생된
**저차원 임베딩(low-dimensional embedding)** 위에 표현되어 있다\[^33].

---

### 인간 신경 활동과의 정렬 (Alignment to human neural activity)

Centaur는 오직 **인간 행동(human behaviour)**에만 맞춰 훈련되었지만,
그 **내부 표현(internal representations)**이
**인간의 신경 활동(human neural activity)**과도 더 잘 정렬되는지 여부에 대해
우리는 궁금증을 가졌다.

이를 확인하기 위해, 우리는 두 가지 분석을 수행하였다.
이들은 모두 **모델의 내부 표현**을 사용하여
**인간의 신경 활동을 예측**하는 방식으로 구성되었다\[^35,^36].

---

#### 전뇌 분석 (Whole-brain analysis)

우리는 먼저 **전뇌 수준의 분석(whole-brain analysis)**을 수행하였다.
이 분석에서는 사람들이 **two-step task**를 수행할 때 측정된
**기능적 자기공명영상(fMRI) 데이터**를 예측하였다\[^37].
이 데이터는 이전 연구에서 수집된 것으로,
**94명의 참가자**가 각각 **300번의 선택**을 수행한 기록을 포함한다.

참가자들은 실험 중
**마법 양탄자 커버 스토리(magic-carpet cover story)** 혹은
**추상적 커버 스토리(abstract cover story)** 중 하나를 접하였다.
이 두 커버 스토리는 모두 Centaur의 훈련 데이터에 포함되지 않았다.

우리는 **각 선택 전(before choice)** 및 **피드백 후(after feedback)** 시점에서
모델의 **레지듀얼 스트림(residual stream)**에서 표현을 추출하였다.
이후 각 뇌 영역(region)에서 인간의 신경 활동을 집계하여
Centaur의 내부 표현에 대해 회귀(regression)를 수행하였다.
이 과정은 각 참가자 및 각 뇌 영역에 대해 **개별적으로 반복**되었다
(Methods, ‘Neural alignment’ 참조).

Fig. 4b는 Centaur와 Llama의 레이어별 Pearson 상관계수(Pearson correlation coefficients)를
측정치(총 n = 11,374)에 대해 평균한 결과를 보여준다.

Centaur의 표현은
Llama의 표현보다 **일관되게 더 높은 예측 성능**을 보였으며
(모든 쌍별 단측 t-검정에서 P ≤ 0.001),
이는 **대규모 행동 데이터(behavioural data)**에 대해
모델을 파인튜닝함으로써
내부 표현이 **인간의 신경 활동과 더 잘 정렬(aligned)**되었음을 시사한다.

주목할 점은, 이러한 분석이 가능한 것은
**Centaur의 표현력(expressivity)** 덕분이며,
**전통적 인지 모델(conventional cognitive model)**의 표현을 사용했을 경우
예측 성능이 **현저히 하락**했다는 것이다 (Fig. 4b의 점선 참고).

더 세부적인 분석 결과는 Extended Data Fig. 6에 제시되어 있다.

---

우리는 이러한 결과를 확장하기 위해,
두 번째 분석을 수행하였다.
여기서는 사람들이 **간단한 6단어 문장(six-word sentences)**을 읽을 때 측정된
**fMRI 데이터**를 활용하였다\[^38].

이 분석의 주된 목적은,
**인지 실험(cognitive experiments)**에 대해 파인튜닝을 수행한 이후에도
**완전히 다른 설정(unrelated settings)**에서의 **신경 정렬(neural alignment)**이
**유지되는지 확인**하는 것이었다.

우리는 **총 5명의 참가자**에 초점을 맞췄으며,
각 참가자는 **1,000개의 문장**을 **수동적으로 읽었고**,
이는 **20개의 실험 세션(run)**과 **2번의 fMRI 스캔 세션**에 걸쳐 수행되었다.
제시된 문장들은 **9개 코퍼스(corpora)**에서 추출되었으며,
**의미적 다양성(semantic diversity)**을 극대화하도록 선별되었다.

우리는 원래 연구의 프로토콜을 면밀히 따르면서,
참가자들의 **언어 네트워크(language network)**에서
집계된 신경 활동(aggregated neural activity)을 예측하였다.

이 예측은 Centaur와 Llama 각각의
**다양한 층(layer)**에서 추출한 표현으로 반복 수행되었다.
그 결과, **대략 20번째 층**에서 **예측력이 최고치에 도달**함을 발견하였다 (Fig. 4c 참조).
이 결과는, 이러한 모델의 **중간층(intermediate layers)**이
가장 많은 정보를 담고 있을 것이라는 가설과 일치한다.

우리는 Centaur와 Llama 간 상관계수 차이에 대해
**역가중 메타 분석(inverse-weighted meta-analysis)**\[^39]을 수행하였고,
그 결과, 전체 층에 걸쳐 **파인튜닝의 유의미한 이점(significant benefit)**이 존재함을 확인하였다:

* β = 0.007
* 95% 신뢰구간: \[0.0002, 0.013]
* P = 0.045

이 효과는 전체 층에 걸쳐 **일관되게 나타났지만**,
**개별 층 수준에서는 통계적으로 유의하지는 않았다**.

---

### 모델 주도 과학적 발견 (Model-guided scientific discovery)

**Psych-101**과 **Centaur**는 모두
**과학적 발견(scientific discovery)**을 위한 **강력한 도구**가 될 수 있다.
이 섹션에서는 이 두 가지가
**인간 의사결정(human decision-making)**에 대한 우리의 이해를
어떻게 향상시킬 수 있는지를 보여주는 **예제(example)**를 제시한다.

그 과정의 개별 단계들은 Fig. 5에 시각적으로 정리되어 있다.

---

**Psych-101**은 인간의 행동 데이터를 **자연어 형식(natural-language format)**으로 포함하고 있다.
이는 **DeepSeek-R1**과 같은 **언어 기반 추론 모델(language-based reasoning model)**이
이를 손쉽게 처리하고 분석할 수 있도록 해준다\[^40].

이를 실제로 시연하기 위해, 우리는 DeepSeek-R1에게
**다속성 의사결정 실험(multi-attribute decision-making experiment)**에서의
참가자 행동에 대한 **설명을 생성해 보라**고 요청하였다\[^41].

이 패러다임에서 참가자는 두 개의 서로 다른 옵션을 제공받으며,
각 옵션은 여러 특성(feature) — 여기서는
**4명의 전문가(experts)의 평가 점수(ratings)** — 로 구성된다.
참가자는 둘 중 어떤 옵션을 선호하는지를 결정해야 한다 (Fig. 5a 참조).

DeepSeek-R1은 여러 설명을 생성하였는데,
그 중 하나가 특히 눈길을 끌었다:

> “참가자는 **2단계 의사결정 전략(two-step decision-making strategy)**을 사용했다.
> 첫째, 모든 전문가의 평가에서 ‘긍정적 평가(1)’를 받은 개수를 비교해
> 더 많은 긍정적 평가를 받은 제품을 선택하였다.
> 둘째, 동점일 경우에는 **신뢰도가 가장 높은 전문가(highest validity expert)**의 평가를
> 기준으로 선택을 결정하였다.”

이 전략은 **두 가지 잘 알려진 휴리스틱 의사결정 전략(heuristic decision-making strategies)**을
결합한 것으로, **우리가 아는 한 기존 연구에서 이러한 조합은 고려되지 않았다.**

이에 따라 우리는 이 **언어 기반 전략(verbal strategy)**을
**형식적 계산 모델(formal computational model)**로 구현하였고,
그 결과 기존 연구에서 고려된 세 가지 전략(가중 가산 방식, 동일 가중치, 대표 선택 휴리스틱)보다
**더 정확하게 인간의 응답 행동을 설명한다**는 것을 확인하였다 (Fig. 5b 참조).

---

그러나 DeepSeek-R1이 발견한 모델의 **Akaike 정보 기준(Akaike Information Criterion, AIC)**은
**181.7**로, Centaur의 AIC **72.5**에 비해 **적합도가 낮았다**.
이로 인해, **개선의 여지(room for improvement)**가 존재함을 알 수 있었다.

우리는 이에 따라 **Scientific Regret Minimization(SRM)**\[^42]이라는 방법을 활용하였다.
이 접근법은 **참조(reference) 모델**로서 **블랙박스 예측 모델(black-box predictive model)**을 사용하며,
특정 계산 모델이 **포착하지 못하는 예측 가능한 응답(responses)**을 찾아내는 데 목적이 있다.

일반적으로 SRM은
해당 실험에 특화된 **대규모 데이터셋(experiment-specific dataset)**을 수집해야 하지만,
Centaur는 **사전 수집된 데이터 없이(out-of-the-box)**도 사용할 수 있기 때문에
이러한 과정을 생략하고도 넓은 범위의 SRM 분석이 가능하다.

실제로 본 사례에서 사용된 **다속성 의사결정 데이터셋**은
**100명 미만의 참가자**를 포함하고 있어,
전통적인 SRM 방식으로는 적용이 어려운 규모였다.

우리는 Centaur는 잘 예측하지만
DeepSeek-R1이 발견한 모델은 **잘 예측하지 못한 응답들**을 검토하였다.
그 결과, 이러한 응답들은 다음과 같은 특성을 갖고 있었다:

> “전체적으로 긍정 평가를 덜 받았음에도 불구하고,
> **신뢰도가 더 높은 전문가(higher-validity expert)**의 긍정 평가를 받은 옵션을
> 참가자가 선택하는 경우.”

이는 DeepSeek-R1이 제시한 전략에서 암시된
**단계적 휴리스틱 전환(either-or heuristic switch)**이
실제로는 그렇게 **엄격하지 않음**을 나타낸다.

이를 반영하여, 우리는 “either-or” 규칙을
**두 휴리스틱의 가중 평균(weighted average)**으로 교체하였다.
그 결과로 생성된 모델은 Centaur와 **동등한 수준의 적합도(goodness-of-fit)**를 보였으며
(AIC = 71.7), 여전히 **해석 가능성(interpretable)**을 유지하였다.

우리는 이렇게 만들어진 모델을 포함하여
모든 후보 모델들의 AIC 값을 **집단 수준 모델 선택(group-level model selection)** 절차에 넣고,
**보호된 초과 확률(protected exceedance probability)**을 추정하였다.
이 값은 해당 모델이 다른 모든 후보들보다
**더 높은 빈도로 사용되었을 확률(probability of highest frequency within the group)**을 의미한다.

그 결과, **SRM 기반 모델의 보호된 초과 확률은 0.83**으로 나타났다.
이러한 결과는, 초기 연구에서 사용된 모델들과 달리
**사람들이 여러 휴리스틱을 조합해서 의사결정을 내린다**는 사실을 보여준다.
즉, 단일한 **가중 가산 전략(weighted-additive strategy)**을 따른다고 보기 어렵다\[^44].

---

### 논의 (Discussion)

본 논문에서는 **Centaur**라는,
**인간 인지(human cognition)**에 대한 **기초 모델(foundation model)**을 제안하였다.
Centaur는 **Psych-101**이라는 **대규모 인간 행동 데이터셋(large-scale dataset of human behaviour)**에 대해,
**최첨단 언어 모델(state-of-the-art language model)**을 **파인튜닝(fine-tuning)**하여 얻어진 결과물이다.

이러한 접근 방식은,
대형 언어 모델(large language models)이 내포한 **방대한 지식(knowledge)**을
활용하는 동시에,
그들을 **인간 행동에 정렬(aligned to human behaviour)**시키는 것을 가능하게 하였다\[^13].

Centaur는 다음을 성공적으로 수행하였다:

* 인간 행동(human behaviour)을 정확히 포착(capture)
* 다양한 **분포 외 설정(out-of-distribution settings)**을 통과(pass)
* 학습에 사용되지 않은 **참가자들(unseen participants)**에 대한 일반화(generalization)
* **커버 스토리(cover stories)**, **구조적 변형(structural variations)**,
    **완전히 새로운 도메인(entirely new domains)**에 대한 일반화

우리는 또한 Centaur를
**행동 수준(behavioural level)**에서 분석했을 뿐만 아니라,
그 **내부 표현(internal representations)**에 대해서도 일련의 분석을 수행하였고,
이를 통해 **인간의 신경 활동(human neural activity)**과의 **정렬 증가(alignment increase)**를 확인하였다.

---

우리는 또한 **사례 연구(case study)**를 통해
**Psych-101**과 **Centaur**가 어떻게
**예측력이 있으면서도 해석 가능한 인지 모델** 개발을 이끌 수 있는지를 시연하였다.
우리가 사용한 개별 단계들은 모두 **일반화 가능한 절차(generic procedure)**이기 때문에,
향후 다른 실험 패러다임들에서도
**모델 주도 과학 발견(model-guided scientific discovery)**의 **청사진(blueprint)**으로 기능할 수 있다.

이러한 예시를 넘어서도,
Centaur는 **자동화된 인지과학(automated cognitive science)**의 맥락에서
다양한 활용 가능성(applications)을 지닌다\[^45,^46].

예를 들어, Centaur는 **in silico 실험 설계(prototyping of experimental studies)**에도 사용할 수 있다\[^47].
이러한 맥락에서 Centaur는 다음과 같은 질문들에 답하는 데 도움을 줄 수 있다:

* 어떤 실험 설계가 가장 큰 **효과 크기(effect size)**를 유도할 수 있을까?
* 참가자 수를 줄이면서도 효과를 유지하려면 어떻게 설계해야 할까?
* 어떤 설계가 효과의 **검정력(statistical power)**을 최대화하는가?

---

Centaur의 **내부 표현(internal representations)**은
**인간의 지식 구조(knowledge structures)**와
**정보 처리 방식(information processing mechanisms)**을 이해하기 위한
새로운 과학적 가설(scientific hypotheses)을 생성하는 데에도 활용될 수 있다.

예컨대, 특정 실험에서
Centaur의 **중간층(intermediate layer)**이 **인간의 신경 반응(human neural responses)**과
가장 높은 정렬도를 보였다면,
이는 해당 층에서 나타나는 **표현 구조(representational structures)**가
실제로 인간의 **인지 처리(cognitive processing)**와 유사하다는 것을 시사할 수 있다.

이러한 경우,
해당 층의 뉴런(예: 토큰 수준 표현, attention 패턴 등)에 대한 정밀 분석을 통해
인간 인지의 **구성 요소(componential structure)**에 대한
**새로운 통찰(insight)**을 도출할 수 있을 것이다.

이는 기존의 **전통적 인지 모델(conventional cognitive models)**이나
**신경과학 모델(neuroscience models)**만으로는
도달하기 어려웠던 새로운 분석 지평을 열어준다.

---

이러한 접근은 특히 **인지신경과학(cognitive neuroscience)** 및
**신경심리학(neuropsychology)** 분야에서 유용할 수 있다.
이들 분야에서는 종종 **실험 설계의 제약(constraints in experimental design)**과
**참가자 수의 한계(small sample sizes)**로 인해
**정량적 모델링(quantitative modelling)**이 어려운 경우가 많다.

Centaur는
**소규모 데이터(small-data regimes)**에서조차
**강력한 사전 정보(strong prior knowledge)**를 제공함으로써,
이러한 분석의 한계를 극복할 수 있다.

예를 들어, **뇌 손상 환자(brain-lesioned patients)**나
**드문 임상 집단(rare clinical populations)**을 대상으로 한 연구에서
Centaur는 **정규 인구(normal population)**에 기반한
행동 및 신경 반응의 **예상 분포(expected distributions)**를 제공함으로써
**편차(deviation)**를 정량화하고 해석하는 데 도움을 줄 수 있다.

---

Centaur 접근은,
**전통적 인지과학(conventional cognitive science)**에서 흔히 사용되는
**모델 구축 방식(model-building approach)**과 근본적으로 다르다.

기존 접근법에서는 다음과 같은 순서를 따른다:

1. **가설(hypothesis)**을 설정한 뒤
2. **계산 모델(computational model)**을 설계하고
3. 이를 **데이터에 적합시켜(fit to data)**
4. **예측 성능(predictive performance)**과 **해석 가능성(interpretability)** 사이에서
     절충(trade-off)을 한다.

반면, Centaur는 다음과 같은 새로운 순서를 제안한다:

1. **정렬된 대규모 모델(aligned large-scale model)**을 먼저 구축한 뒤
2. 이를 사용해 **현존하지 않는(hypothetical)** 또는 **불명확한** 인지 전략을 탐색하고
3. 이로부터 도출된 전략을 바탕으로 **형식적 계산 모델(formal computational model)**을 구성하며
4. 이 모델이 **해석 가능성**과 **예측 성능**을 모두 만족하도록 정제(refinement)해간다.

이 방식은 **이론 생성(theory generation)**을
더욱 **경험적(empirical)**이고 **자동화된 절차(data-driven, automated process)**로 바꾸는 것을 목표로 한다.

---

요약하자면, 우리는 다음 두 가지를 통해
**인간 인지의 기초 모델(foundation model of human cognition)**을 구축하였다:

1. **대규모 인간 실험 데이터셋(large-scale dataset of human experiments)**인 **Psych-101**,
2. 이 데이터셋을 기반으로 파인튜닝된 **언어 모델(language model)**인 **Centaur**.

Centaur는 단순히 인간 행동을 예측하는 것을 넘어서,
**인간의 신경 활동(human neural activity)**과 **정렬(alignment)**되며,
**과학적 발견(scientific discovery)**을 도울 수 있는
**해석 가능한 이론(interpretable theories)**을 생성해낼 수 있다.

우리는 이 연구가
**인지과학(cognitive science)**, **심리학(psychology)**,
그리고 **신경과학(neuroscience)** 전반에 걸쳐
**새로운 시대(new era)**를 여는 계기가 되기를 기대한다.

