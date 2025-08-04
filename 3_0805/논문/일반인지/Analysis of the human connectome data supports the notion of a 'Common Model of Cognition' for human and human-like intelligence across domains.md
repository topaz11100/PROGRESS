**"Analysis of the human connectome data supports the notion of a 'Common Model of Cognition' for human and human-like intelligence across domains" (NeuroImage, 2021)**

---

## 초록 (Abstract)

**공통 인지 모델(Common Model of Cognition, CMC)**은 인간 및 인간 유사 지능(human-like intelligence)을 모델링하는 데 있어 인지과학(cognitive science) 분야의 수십 년간의 진전을 포괄하는 것을 목적으로 제안된 최근의 합의 기반 아키텍처이다. 이 모델에 대한 광범위한 합의와 해당 구성요소들을 특정 뇌 영역에 사전 매핑한 결과를 바탕으로, 우리는 **CMC**가 인간 뇌의 대규모 기능 아키텍처(large-scale functional architecture)의 유력한 후보 모델이 될 수 있다는 가설을 세웠다. 이 가설을 검증하기 위해 우리는 7개의 다양한 인지 영역(cognitive domains)을 포괄하는 과제를 수행한 200명의 참가자로부터 얻은 기능적 자기공명영상(functional MRI, fMRI) 데이터를 분석하였다.

**CMC**의 구성요소들은 정준 fMRI 분석(canonical fMRI analysis)을 통해 기능적으로 상동적인 뇌 영역(functionally homologous brain regions)과 연관지어졌으며, 이들 간의 연결 경로는 영역 간의 유효 연결성(effective connectivity) 패턴으로 번역되었다. 결과로 생성된 동적 선형 모델(dynamic linear model)은 **동적 인과 모델링(Dynamic Causal Modeling, DCM)**을 이용해 구현 및 적합(fit)되었으며, 뇌과학(neuroscience) 분야에서 이전에 제안된 6개의 대체 아키텍처(3개의 계층적 아키텍처(hierarchical architectures)와 3개의 중심-주변(hub-and-spoke) 아키텍처)와 비교되었다. 이 비교는 **베이지안(Bayesian) 접근법**을 통해 수행되었다.

분석 결과는 모든 경우에서 **CMC**가 각 영역 내(task-specific)뿐 아니라 모든 과제 전반에 걸쳐(task-general) 다른 모든 아키텍처들보다 성능이 훨씬 우수함을 보여준다. 이러한 결과는, 인공지능(artificial intelligence)을 위한 공통의 구조적 원칙이 인간의 다양한 인지 영역 전반에서도 똑같이 인간 뇌 기능의 기저를 이루고 있다는 점을 시사한다.

---

## 1. 서론 (Introduction)

복잡한 시스템의 기본적인 조직 원리(organizational principle)는 흔히 그 시스템의 **아키텍처(architecture)**라고 불리며, 시스템의 기능(function)과 구조(structure) 간의 관계를 이해하기 위한 중요한 개념적 도구로 작용한다. 예를 들어, **폰 노이만 아키텍처(von Neumann architecture)**는 현대 디지털 컴퓨터의 조직 원리를 설명하며, 이는 특정 마더보드(motherboard)의 배선을 무시하고 계산 이론(theory of computation)에 대응시키는 방식으로 컴퓨터를 기능적 수준(functional level)에서 설명하거나, 또는 복잡한 하드웨어의 문제를 진단하는 데 사용할 수 있다 (즉, 마더보드의 구성요소 및 그 배선의 기능을 식별함으로써 진단이 가능하다).

인간 뇌(human brain)의 놀라운 복잡성은 이와 유사하게 **뇌 아키텍처(brain architecture)**를 찾고자 하는 시도를 촉진시켜 왔으며, 이는 마치 폰 노이만 아키텍처처럼 뇌의 구성 요소들을 그 기능적 특성과 연관 짓는 모델이다. 이러한 탐색이 성공한다면, 뇌 기능 및 기능 장애(dysfunction)에 대한 보다 근본적인 이해를 제공할 수 있으며, 나아가 인공지능(artificial intelligence) 개발을 위한 새로운 원리를 도출할 수 있을 것이다 (Hassabis et al., 2017).

이와 같은 방향의 대부분의 시도는 **하향식(bottom-up)** 접근 방식이었다. 즉, 대규모 연결성 데이터(connectivity data)에 차원 축소(dimensionality-reduction) 및 머신러닝(machine learning) 기법을 적용하여 기능적으로 연결된 영역들(clusters of functionally connected areas)을 식별하는 데 중점을 두었다 (예: Cole et al., 2013; Porgolewski et al., 2014; Huntenburg et al., 2018). 이러한 모델들은 과제(task) 관련 뇌 활동을 예측하는 데 활용될 수 있지만, 대규모 연결성에 의존하며 각 네트워크 노드의 기능에 대해서는 근본적으로 **불가지론적(agnostic)**이거나(최선의 경우) **과제 특화적 추정(task-specific guess)**에 의존한다. 이러한 접근은 또한 사용된 데이터의 유형 및 적용된 분석 방법에 따라 결과가 달라질 수 있다. 예를 들어, 어떤 연구자는 특정 과제 기반 fMRI(task-based fMRI) 및 여러 뇌 영역 간 활동의 동시 발생(co-occurrence)을 기반으로 기능적 지표에 집중하는 반면, 또 다른 연구자는 자발적 활동(resting-state activity) 및 저주파 시계열 상관관계(slow frequency time series correlation)에 초점을 맞출 수 있다.

최근 지적되었듯이 (Jonas and Kording, 2017), 이러한 방법들 중 어느 것도 데이터로부터 기능적 설명(functional explanation)을 보장하지는 않는다. 그러나 동일한 방법들을 활용하여 **두 개 이상의 모델을 데이터에 대해 검증(test)**하는 **상향식(top-down)** 접근법에서는 성공적으로 사용할 수 있다 (Jonas and Kording, 2017). 다시 말해, 특정 뇌 기능 모델이 주어졌을 때, 전통적인 연결성 분석(connectivity analysis)은 그 모델이 실제 데이터에 얼마나 잘 부합하는지를 판단하고 다른 모델들과 비교 평가하는 데 신뢰할 수 있는 답을 제공할 수 있다. 단, 이러한 **상향식(top-down)** 접근법은 **이론적 근거(theoretically-motivated)**를 갖춘 유력한 기능 모델(functional model)을 전제로 해야 한다.

---

### 1.1 공통 인지 모델 (The Common Model of Cognition, CMC)

유력한 후보로 떠오른 하나의 제안은 **공통 인지 모델(Common Model of Cognition, CMC)**이다 (Laird et al., 2017). 이름에서 알 수 있듯이, CMC는 인지심리학(cognitive psychology), 인공지능(artificial intelligence), 그리고 로보틱스(robotics) 분야에서 지난 50여 년간 개발된 다양한 인지 아키텍처(cognitive architectures)들의 유사성을 요약한 **공통의 조직 원리 집합(common set of organizing principles)**이다. 이는 일반 지능(general intelligence)을 위한 아키텍처이며, 그 의미는 CMC 원리에 기반한 에이전트(agent)는 특정한 좁은 영역에서의 최적 행동(optimal behavior)이 아니라, **도메인 전반에 걸쳐 합리적이고 적응적인 행동(rational and adaptive behavior across domains)**을 보여야 한다는 것이다.
¹ 여기서 말하는 **‘일반 지능’(general intelligence)**은 심리측정(psychometrics)에서 사용되는 ‘g 요인(g factor)’—즉 서로 다른 과제들 간의 수행 상관관계를 설명하는 가설적 요소—과는 다른 개념이다 (Hunt, 2010). 이 두 정의 간의 관계와 추가 정의들에 대해서는 Legg & Hutter (2007)를 참조할 수 있다.

CMC는 그 일반성과 합의 가능성 때문에 **인지 에이전트 설계의 지침**으로 널리 사용되고 있다 (예: Mohan, n.d.). CMC에 따르면, 인간 수준의 지능(human-like intelligence)을 갖는 에이전트들은 다음과 같은 다섯 개의 기능 구성요소(functional components)를 공유한다:

1. **특징 기반의 선언적 장기기억(declarative long-term memory)**
2. **버퍼 기반의 작업 기억(buffer-based working memory)**
3. **절차적 기억(procedural memory)**에 표현된 행동(action)을 **패턴 기반으로 호출(pattern-directed invocation)**하는 시스템
4. **지각(perception) 시스템**
5. **행동(action) 시스템**

이 중 **작업 기억(working memory)**은 중심 허브(hub)의 역할을 하며, 다른 모든 구성요소는 이를 통해 소통한다. 단, 지각과 행동 사이에는 별도의 직접 연결(direct connection)이 존재한다(그림 1A 참조). 또한 CMC는 각 구성요소의 기능적 특성(functional properties)을 규정하는 **표현 방식과 처리 메커니즘에 대한 제약조건**도 함께 포함한다.

CMC의 구성요소와 전제들은 지난 50년간 **일반적인 인간 수준 능력을 지닌 인지적 컴퓨터 모델(computational cognitive models)** 및 **인공 에이전트(artificial agents)**를 개발하는 과정에서 축적된 지식들을 요약한 것이다. 놀랍게도, 이러한 지식들은 적용 분야에 상관없이 일관되게 등장한다. 예를 들어, 인지 아키텍처 **Soar** (Laird, 2012)는 자율 인공 에이전트 및 로봇 설계에 주로 사용되고, **ACT-R** (Anderson, 2007)은 심리학 실험의 시뮬레이션 및 인간 행동 예측에 주로 사용되지만 (Kotseruba and Tsotsos, 2020), 이들 모두가 **CMC의 핵심 가정들**에 독립적으로 수렴하였다 (Laird et al., 2017).

비슷한 맥락에서, 대규모 뇌 모델인 **SPAUN** (Eliasmith et al., 2012)과 **Leabra 신경 아키텍처(Leabra neural architecture)** (O’Reilly et al., 2016) 또한 서로 다른 전제(예: 뉴런 부호화 방식, 표현 방식, 학습 알고리즘)를 바탕으로 설계되었지만, **작업 기억, 절차적 기억, 장기 기억** 등과 같은 고수준 모듈의 존재에 대해서는 **CMC와 유사한 구성**을 갖는다.

최신 인공신경망 기반 AI 시스템도 어느 정도 이러한 동일한 구성요소들을 채택한다. 예를 들어, DeepMind의 **AlphaGo**는 다음과 같은 요소를 포함한다:

* **몽테카를로 트리 탐색(Monte-Carlo tree search)** 기반의 계획 및 탐색 구성요소 (작업 기억에 해당)
* **정책 네트워크(policy network)** (절차적 기억에 해당)
* 별도로 설계된 **지각 및 행동 시스템(perception and action systems)**

(출처: Silver et al., 2016)

또한, **Differentiable Neural Computer** (Graves et al., 2016)는 외부 메모리(external memory)에 접근하는 최적 정책(optimal policies)을 학습하는 절차적 기억과, 기호 기반 장기 기억(symbolic long-term memory)을 포함한다.

이처럼, CMC는 인간 유사한 유연성과 지능을 달성하도록 설계된 시스템들이 일반적으로 따르는 구성 원리를 반영하며, **인간 두뇌에도 적용 가능할 가능성**이 있다. 따라서 CMC는 **상향식(top-down)** 방식으로 뇌 아키텍처를 탐색하는 데 이상적인 이론적 후보로 간주된다.

---

### 1.2 뇌 아키텍처로서 CMC를 평가하기 (Assessing the CMC as a brain architecture)

**CMC(Common Model of Cognition)**가 유효한 후보 모델이라면, 그것이 **인간 뇌 아키텍처(human brain architecture)**로서의 타당성을 갖는지를 어떻게 평가할 수 있을까? 실용적인 차원에서, 하나의 유망한 아키텍처는 두 가지 기준을 충족해야 한다:

1. **보편성 기준(Generality criterion)**: 동일한 인지 아키텍처가 다양한 영역과 과제를 아우르는 뇌 활동(brain activity) 데이터를 설명할 수 있어야 한다.
2. **비교적 우수성 기준(Comparative superiority criterion)**: 해당 아키텍처는 유사한 복잡도와 일반성을 가진 경쟁 아키텍처들과 비교했을 때 **실험적 뇌 데이터에 대해 더 우수한 적합도(fit)**를 보여야 한다.

이 두 가지 기준에 대해 CMC를 검증하기 위해, 우리는 **Human Connectome Project(HCP)**에서 수집된 **200명의 젊은 성인 참가자**의 **과제 기반 기능적 뇌영상(task-related functional neuroimaging)** 데이터를 종합적으로 분석하였다. HCP는 현재까지 존재하는 가장 고품질의 인간 신경영상 데이터 저장소이며, fMRI 및 MEG 데이터를 포함하지만, 본 연구에서는 **subcortical source**(CMC에서 매우 중요한 요소)를 명확히 식별할 수 있는 **fMRI 데이터만을 사용**하였다. MEG는 이러한 식별이 어려워 분석에서 제외되었다.

HCP 데이터는 참가자들이 수행한 7개의 심리학적 과제를 포함하며, 이 과제들은 모두 **기존 신경영상 연구에서 사용된 대표적 과제들**을 기반으로 구성되었고, **인간 인지의 다양한 범위**를 포괄할 수 있도록 선정되었다 (Van Essen et al., 2013). 구체적으로, 이 과제들은 다음과 같은 영역들을 포함한다:

* 언어 처리(language processing) 및 수리 인지(mathematical cognition) (Binder et al., 2011)
* 작업 기억(working memory)
* 보상 기반 의사결정(incentive processing and decision making) (Delgado et al., 2000)
* 감정 처리(emotion processing) (Hariri et al., 2002)
* 사회 인지(social cognition) (Wheatley et al., 2007)
* 관계 추론(relational reasoning) (Smith et al., 2007)

이 7개 과제는 총 6가지 실험 패러다임(paradigm)을 구성하며, 언어와 수리 인지는 동일한 패러다임 내에서 테스트되었다.

CMC를 하나의 **뇌 네트워크 아키텍처(brain network architecture)**로 변환하려면, 그 다섯 개의 구성요소를 **기능적으로 유사하면서도 공간적으로 구분 가능한(functionally homologous and spatially localized)** 뇌 영역에 대응시켜야 한다. 인간 뇌에서 해부학적으로 식별 가능한 영역의 수는 수백 개에 달하지만 (Glasser et al., 2016; Power et al., 2011; Yeo et al., 2011), 이러한 해부학적 영역의 수는 기능적 구분의 기준으로는 지나치게 세분화되어 있다. 대신, **기능적으로 구별되는 회로(functionally distinct circuits)**의 수는 최소한 **그보다 한 자릿수(order of magnitude) 작다**는 것이 일반적인 견해이며, 뇌는 다양한 영역이 상호 연결된 **기능 네트워크(functional networks)**를 형성한다 (Cole et al., 2016; Power et al., 2011; Yeo et al., 2011).

본 연구는 이러한 논의를 바탕으로, Yeo et al. (2011)에서 제시한 영향력 있는 분류를 참조점으로 사용한다. 이 분류는 총 **7개의 기능 네트워크**를 식별하며, 이는 CMC 구성요소 수와 유사한 수준이다.

따라서 초기 식별 단계에서는 CMC 구성요소와 일부 기능 네트워크 사이에 다음과 같은 일대일 대응을 설정하였다. 이 대응은 문헌에 기초한 것이며, ACT-R의 모듈별 버퍼(module-specific buffers)나 대규모 뇌 모델(예: Eliasmith et al., 2012; O'Reilly et al., 2016)에서 제안된 기능-구조 매핑(function-to-structure mappings)과도 일치한다:

* **작업 기억(working memory)** → 전두-두정 네트워크(fronto-parietal network): 배외측 전전두피질(dorsolateral prefrontal cortex, PFC)과 후두정피질(posterior parietal cortex)
* **장기 기억(long-term memory)** → 에피소드 기억과 관련된 영역들: 해마(hippocampus) 및 내측 측두엽(medial temporal lobe), 기억 회상에 관련된 내측 전두피질(medial frontal cortex)과 precuneus; 즉 **디폴트 모드 네트워크(default mode network)** (Raichle and Snyder, 2007)
* **행동(action)** → 감각운동 네트워크(sensorimotor network) (Power et al., 2011)
* **절차적 기억(procedural knowledge)** → 기저핵(basal ganglia) (Yin and Knowlton, 2006)
* **지각(perception)** → 등쪽(dorsal) 및 복측(ventral) 시각 네트워크, 과제에 따라 청각 네트워크도 포함 가능 (그림 1B 참조)

이러한 매핑을 바탕으로, 본 연구는 **각 과제 및 각 참가자마다 개별적인 ROI(region of interest)를 정의하기 위한 분석 파이프라인**을 설계하였다. 이로써 개인별 기능적 신경해부학(functional neuroanatomy)의 차이를 반영할 수 있게 하였다 (그림 1C; 세부 내용은 Materials & Methods 참조).

---

### 1.3 대안 아키텍처 (Alternative architectures)

**비교적 우수성 기준(Comparative superiority criterion)**을 충족하기 위해, 본 연구는 **CMC(Common Model of Cognition)** 연결성 모델(connectivity model)을 **대안적 연결성 모델(alternative connectivity models)**들과 비교하였다. 이들 대안 모델은 **이전에 신경과학(neuroscience) 문헌에서 제안된 이론적 뇌 아키텍처(theoretical brain architectures)**를 대표하는 모델들이다 (그림 2 참조). 가능한 모델의 공간(model space)은 매우 크기 때문에, 본 연구는 기존 문헌에서 자주 등장한 여섯 가지 대표적 사례에 초점을 맞췄다.

이 여섯 가지 대안은 두 가지 계열(family)로 나눌 수 있다:

---

#### ▶️ 계층적 아키텍처 계열 (Hierarchical family)

이 계열에서의 뇌 연결성(brain connectivity)은 **지각(Perception)**에서 시작해 **행동(Action)**으로 종결되는 **처리의 계층적 수준(hierarchical levels of processing)**을 구현한다. 즉, 이 구조는 뇌를 **대규모 추상화 수준의 feedforward 신경망 모델(feedforward neural network with large-scale gradients of abstraction)**로 개념화하는 것이다 (Huntenburg et al., 2018).

이러한 계층 구조 내에서, 각 **ROI(region of interest)**는 서로 다른 처리 수준을 나타내며, 그 아래 수준의 ROI로부터 **상향 연결(forward projection)**을 받고, 위 수준의 ROI로는 **하향 연결(backward projection)**을 보낸다. 여기서 모델 설계의 자유도(degree of freedom)는 계층 내에서 구성요소들의 **정렬 순서(ordering)**에 있다.

단, 지각(Perception)은 항상 입력(input), 행동(Action)은 항상 출력(output)으로 고정되며, **작업 기억(working memory, WM)**은 **장기 기억(long-term memory, LTM)**보다 더 높은 수준으로 간주된다. 이러한 제약 아래, 유일한 자유도는 **절차적 기억(procedural region)**이 계층 내에서 어디에 위치하는가에 있으며, 이에 따라 세 가지 계층적 아키텍처가 도출된다 (그림 2B):

1. **계층형 아키텍처 1 (Hierarchical 1)**: 절차적 영역이 지각과 장기 기억 사이에 위치
    → 이는 지각 범주화(perceptual categorization)에서의 기저핵(basal ganglia) 모델에 기반 (Ashby et al., 2007; Kotz et al., 2009; Seger, 2008)

2. **계층형 아키텍처 2 (Hierarchical 2)**: 절차적 영역이 장기 기억과 작업 기억 사이에 위치
    → 이는 기억 회상(memory retrieval)에서의 기저핵 역할을 반영 (Scimeca and Badre, 2012; Tricomi and Fiez, 2012)

3. **계층형 아키텍처 3 (Hierarchical 3)**: 절차적 영역이 작업 기억과 행동 사이에 위치
    → 이는 운동 제어(motor control)에서의 기저핵 모델에 기반 (Houk et al., 2007)

---

#### ▶️ 중심-주변 아키텍처 계열 (Hub-and-Spoke family)

이 계열에서는 단일 ROI가 네트워크의 **중심 허브(Hub)** 역할을 하며, 다른 모든 ROI들(Spokes)과 **양방향 연결(bidirectional connections)**을 가진다. 단, 중심 허브를 제외한 어떠한 ROI도 서로 직접 연결되지 않는다 (그림 2C).

CMC에서는 작업 기억(WM)이 중심 허브 역할을 하기 때문에, 이와 유사한 방식으로 세 가지 중심-주변 아키텍처가 설정되었다. 중심 허브로 선택된 영역은 다음과 같다 (단, 지각과 행동은 허브로 선택되지 않음):

1. **Hub-WM 모델**: 허브 역할은 작업 기억(WM)이 수행
    → WM은 전두엽 피질(lateral prefrontal cortex, PFC)로 매핑되며, **PFC를 유연한 제어 허브(flexible control hub)**로 보는 관점과 일치 (Cole et al., 2012, 2013)
    → 네트워크 구조 측면에서 **CMC와 가장 유사**하며, 둘 다 중심 허브로 WM을 두고, 추가로 **지각-행동 간 직접 연결**이 있음

2. **Hub-Procedural 모델**: 허브 역할은 절차적 기억(procedural memory)이 수행
    → 이는 생산 규칙 기반 인지 아키텍처(cognitive architectures based on production systems)에서 절차적 제어의 중심성을 반영 (Anderson, 2007; Kieras and Meyer, 1997; Laird, 2012)
    → 절차적 기억은 기저핵(basal ganglia)으로 매핑되며, 이 모델은 **행동 선택(action selection)** 및 **피질 활동 조정(cortical coordination)**에서의 기저핵의 중심성을 반영 (Eliasmith et al., 2012; Hazy et al., 2007; Stocco et al., 2010)

3. **Hub-LTM 모델**: 허브 역할은 장기 기억(LTM)이 수행
    → 이는 감각 및 에피소드 정보가 의미적으로 통합되어 지각을 해석하고 행동을 안내한다는 **‘허브-주변’ 의미론 모델(hub-and-spoke semantic model)**의 관점에서 비롯됨 (Chiou and Lambon Ralph, 2016; Rogers et al., 2004)

---

이처럼 정의된 여섯 가지 대안 아키텍처는 제안된 제약 조건 하에서 가능한 **계층형 및 중심-주변형 구성의 모든 조합**을 포괄한다. 이들 모델은 모두 **뇌 아키텍처의 대규모 개념 청사진(conceptual blueprint)**으로서 다섯 가지 CMC 구성요소를 어떻게 조직할지를 보여주는 대표적 사례들이며, 단지 구성요소 간 어떤 연결이 더 근본적인지를 다르게 선택할 뿐이다.

이 모든 아키텍처는 기존 문헌에서 **뇌 조직을 해석하기 위한 그럴듯한(plausible) 모델**로 제안된 바 있으며, **CMC 대비 극단적으로 다른 형태는 아니다.** 실제로, 이들 모델은 **CMC에서 최대 6개의 연결만 변경함으로써 쉽게 생성**될 수 있으며 (그림 2B–C에서 회색 점선 및 빨간색 화살표로 표시됨), 따라서 **모델 복잡도(network complexity)** 차이로 인한 적합도 차이가 발생할 가능성은 낮다.

---

### 1.4 네트워크 동역학 모델링 (Modeling network dynamics)

**ROI(Region of Interest)** 네트워크와 이들 간의 신경 활동 간의 연관성은 **동적 인과 모델링(Dynamic Causal Modeling, DCM)** 기법을 통해 제공되었다 (Friston et al., 2003). DCM은 **신경 집단 기반 수리 모델(neuronal-mass mathematical modeling technique)**로, 일련의 외부 자극(external drives)에 반응하는 뇌 영역 간 활동의 시간 흐름(time-course)을 동적 시스템(dynamic system)으로 근사한다.

보다 구체적으로, ROI 집합의 **기저 신경 활동(neural activity) y**의 시간 흐름은 다음과 같은 **이차 선형 상태 변화 방정식(bilinear state change equation)**으로 기술된다:

$$
\frac{dy}{dt} = Ay + \sum_i x_i B_i y + Cx
$$

여기서,

* **x**: 실험 이벤트 벡터(event vectors), 즉 전통적 GLM(General Linear Model) 분석의 디자인 매트릭스에 해당
* **A**: ROI 간의 **내재적 연결성(intrinsic connectivity)**
* **C**: 과제 이벤트(task events)의 ROI별 직접 효과
* **B**: 과제 조건(task conditions)이 ROI 간 연결에 미치는 **조절 효과(modulatory effects)**

단순화를 위해, 본 연구에서는 **B 행렬을 0으로 설정**하여 조절 효과를 제외하였고, 따라서 위 식은 다음과 같이 축약된다:

$$
\frac{dy}{dt} = Ay + Cx
$$

이렇게 시뮬레이션된 신경 활동 **y**로부터, 생물학적으로 타당한 모델을 적용하여 **예측 BOLD 신호(BOLD: Blood Oxygenation Level Dependent)**의 시간 흐름을 생성하였다. 이때 사용된 모델은 **"풍선 모델(balloon model)"**이라 불리는 **신경-혈관 결합(neurovascular coupling)** 모델이다 (Buxton et al., 1998; Friston et al., 2000).

DCM 기법을 선택한 이유는 다음과 같다:

1. **모델 설계, 적합(fit), 평가**를 위한 통합 프레임워크가 존재함
2. 전통적 기능 연결성 분석(functional connectivity analysis)과 달리, **네트워크 내 방향성(directionality) 효과를 추정할 수 있음**
3. Granger 인과성 분석(Granger causality)과 달리, **신경 동역학 모델링과 영상 신호 모델링을 구분**하여 수행하며, 이를 통해 동일한 신경 모델을 다양한 측정 방식(M/EEG 등)에 적용할 수 있음

---

## 2. 재료 및 방법 (Materials and Methods)

본 연구는 **Human Connectome Project (HCP)**로부터 수집된 **대규모 신경영상 데이터 샘플(N = 200)**을 광범위하게 분석한 것이다. HCP는 현재 존재하는 가장 큰 규모의 **젊은 성인(young adult)** 대상 **신경영상 데이터 저장소(neuroimaging repository)**이다.

본 연구의 분석은 다음 데이터를 제외하고 **과제 기반 fMRI(task-based fMRI)** 데이터에만 국한되었다:

* **안정 상태 fMRI(resting-state fMRI)**
* **확산 영상(diffusion imaging)**
* **M/EEG(자기뇌파 및 뇌전도)** 데이터

HCP의 과제 기반 fMRI는 다음을 포함한다:

* **7개의 실험 패러다임(paradigm)**, 각 패러다임은 서로 다른 인지 영역(cognitive domain)을 측정하도록 설계됨
* 각 패러다임에 대해 **두 번의 세션을 실시**

참가자 모집 절차 및 **동의서(informed consent)**는 모두 **워싱턴 대학교 세인트루이스 캠퍼스(Washington University in St. Louis)**의 **IRB(Institutional Review Board, 기관생명윤리위원회)**의 승인을 받았다.
현재 논문은 **워싱턴 대학교 시애틀 캠퍼스(University of Washington)**의 IRB에서 **면제 기준에 해당하는 연구**로 승인되었다.

---

### 2.1 과제 기반 fMRI 데이터 (Tasks fMRI data)

HCP의 과제 기반 fMRI 데이터는 인간의 다양한 인지 능력(cognitive capabilities)을 포괄하도록 설계된 **7가지 서로 다른 실험 패러다임**을 포함하고 있다. 이 중 본 연구에서는 **6가지 패러다임**만을 분석 대상으로 삼았으며, **운동 매핑(Motor Mapping)** 과제는 제외하였다.
운동 매핑 과제의 제외 이유는 다음과 같다:

* 손, 팔, 다리, 목소리 등 **각 운동 부위에 대해 별개의 motor ROI(region of interest)**를 생성해야 하며,
* 이러한 다중 ROI 요구는 **다른 과제들과 본질적으로 모델 구조가 달라지는 결과**를 낳기 때문

각 과제의 상세 설명과 선정 이유는 HCP의 원 논문들 (Barch et al., 2013; Van Essen et al., 2013)을 참조. 본 논문에서는 간략한 설명만 제공하며, 요약 정보는 아래의 **Table 1**에 정리되어 있다.

---

#### ▶ 감정 처리 과제 (Emotion Processing Task)

* 참가자에게 **총 12개의 블록**이 제시됨 (각 블록: 6개의 연속된 시도(trial)로 구성)
* 각 시도에서는, 참가자는 화면 하단의 두 시각 자극 중에서 **화면 상단 자극과 일치하는 것**을 선택해야 함
* 6개의 블록: **분노 혹은 공포 표정의 얼굴들** 사용
* 나머지 6개 블록: **중립 도형(neutral shapes)** 사용
* 각 자극: 2초간 제시, 시도 간 간격(inter-trial interval, ITI): 1초
* 각 블록 시작 전, 과제 유형(“shape” 또는 “face”)을 나타내는 **3초간의 큐(cue)**가 포함됨
* 블록 총 길이: **21초**

#### ▶ 보상 처리 과제 (Incentive Processing Task)

* 참가자는 **총 4개 블록(각 8개의 연속 시도)**에 참여
* 각 시도: 참가자는 **“?”로 표시된 카드** 아래의 숫자가 5보다 큰지 작은지를 추측하여 버튼을 누름
* 응답 후 실제 숫자가 공개되며, 다음과 같은 보상 구조가 적용됨:
   ✓ 정답 → +\$1.00
   ✓ 오답 → -\$0.50
   ✓ 숫자 = 5 → 0 (보상 없음)
* 각 블록은 **실제로는 미리 설정된 승리(high-reward) 또는 손실(high-loss)** 블록 (참가자에게는 비공개)
* 각 자극: 최대 1.5초, 피드백: 1초, ITI: 1초 → 블록 총 길이: **27초**

#### ▶ 언어 및 수학 과제 (Language and Mathematical Processing Task)

* 총 **4개의 이야기(story) 블록**과 **4개의 수학(math) 블록**이 교차로 제시됨
* 두 블록 모두 동일한 구조를 가짐:
   ① 청각 자극으로 제시되는 짧은 이야기 또는 계산 문제
   ② 이어서 제시되는 **양자택일형 질문(two-alternative question)**에 응답 (버튼 클릭)
* 이야기 자극: 이솝우화(Aesop's fables)를 기반으로 간결하게 각색됨 (5\~9문장)
* 수학 자극: 예) “14 더하기 12는?”, 질문: “26인가 29인가?”
* 수학 블록은 참가자 별 난이도 조절을 통해 유사한 난이도를 유지함

---

#### ▶ 관계 추론 과제 (Relational Processing Task)

* 총 **6개의 관계(Relational) 블록**과 **6개의 통제(Control) 블록**으로 구성

* **Relational 블록**: 두 쌍의 그림이 제시됨
   · 하나는 화면 상단 수평 방향,
   · 다른 하나는 화면 하단 수평 방향
   · 각 그림은 총 36개의 조합 중 하나로 구성됨 (6종의 도형 × 6종의 텍스처)
   · 각 쌍은 한 가지 차원(도형/텍스처)에서만 차이남
   → 참가자는 상단 쌍과 하단 쌍이 동일한 차원에서 차이를 보이는지를 판단

* **Control 블록**:
   · 상단에 도형 쌍 하나, 하단 중앙에 도형 하나,
   · 중앙에 단어 자극(“shape” 또는 “texture”) 제시
   → 참가자는 하단 도형이 상단 도형 둘 중 하나와 해당 차원에서 일치하는지 판단

* 두 블록 모두 총 길이는 **16초**
   · Relational 블록: 4개의 자극 × 3.5초, ITI(간격): 500ms
   · Control 블록: 5개의 자극 × 2.8초, ITI: 400ms

---

#### ▶ 사회 인지 과제 (Social Cognition Task)

* 참가자는 **총 10개의 짧은 동영상 클립**을 시청

* 도형(원, 사각형, 삼각형)이 움직이는 장면이 포함됨
   · 5개의 클립: 도형이 무작위로 움직임 (random motion)
   · 5개의 클립: 도형이 **사회적 상호작용(social interaction)**을 나타냄
   → 예: 쫓기, 따라가기, 협력 등

* 클립 시청 후, 참가자는 버튼 3개 중 하나를 눌러 응답:
   ① 상호작용함
   ② 상호작용 안 함
   ③ 잘 모르겠음

* 각 클립 길이: **20초**, 자극 간 간격(ITI): **15초**

---

#### ▶ 작업 기억 과제 (Working Memory Task)

* 총 **8개의 2-back 블록**과 **8개의 0-back 블록**으로 구성

* 각 블록은 **10개의 시도(trials)**로 구성

* **2-back 블록**:
   · 참가자는 현재 자극이 **두 단계 전 자극과 동일한지 여부** 판단
   → 즉, 두 개의 자극을 지속적으로 기억하며 갱신해야 함
   → 고부하 작업 기억 요구

* **0-back 블록**:
   · 블록 시작 시 하나의 **기준 자극(target)** 제시됨
   · 이후 자극이 기준 자극과 같은지만 판단 → 기억 부하 낮음

* 사용된 자극 종류: 총 4가지 범주
   ① 얼굴(faces)
   ② 장소(places)
   ③ 도구(tools)
   ④ 신체 부위(body parts)
   → 각 블록은 한 가지 범주만 포함하며, 모든 조건에서 각 범주가 고르게 분포

* 각 블록은 다음과 같은 구조를 가짐:
   · 시작: 2.5초간 블록 유형 큐(“2-back” 또는 “0-back”) 제시
   · 각 자극: 2초
   · 자극 간 간격(ITI): 500ms
   → 총 블록 길이: **27.5초**

---

## 2.2 데이터 처리 및 분석 (Data Processing and Analysis)

### ▶ 영상 획득 매개변수 (Imaging Acquisition Parameters)

Barch et al. (2013)의 보고에 따르면, 기능적 뇌영상(fMRI)은 다음과 같은 조건으로 획득되었다:

* **3 테슬라 Siemens Skyra 장비** 및 **32채널 두부 코일(head coil)** 사용
* 반복 시간 (TR): 720 ms
* 에코 시간 (TE): 33.1 ms
* 플립 각도 (FA): 52도
* 시야(FOV, field of view): 208 × 180 mm
* 각 이미지는 두께 2.0 mm의 **72개 경사 슬라이스(oblique slices)**로 구성되며 슬라이스 간 간격은 0 mm
* 평면 내 해상도: 2.0 × 2.0 mm
* **멀티밴드 가속도(multiband acceleration factor)**: 8배

---

### ▶ 영상 전처리 (Image Preprocessing)

영상은 HCP에서 제공하는 **“최소 전처리(minimally preprocessed)”** 형식으로 사용되었으며, 여기에는 다음 단계가 포함된다 (Van Essen et al., 2013):

* 자기장 왜곡 보정 (unwarping)
* 움직임 재정렬 (motion realignment)
* MNI 표준 템플릿으로 정규화 (normalization)

이후 모든 영상은 **등방성 8.0 mm FWHM 가우시안 커널**로 **공간 평활화(spatial smoothing)**되었다.

---

### ▶ 정준 GLM 분석 (Canonical GLM Analysis)

정준 범용 선형 모델(General Linear Model, GLM) 분석은 평활화된 최소 전처리 데이터에 대해 **mass-univariate 방식**으로 수행되었으며, **SPM12 소프트웨어**를 사용하였다 (Penny et al., 2011).

* **1단계(개인 수준)**: 각 참가자에 대해 개별 모델 생성
   · 디자인 매트릭스는 각 실험 조건의 타이밍 정보를 기반으로 **헤모다이나믹 반응 함수(hemodynamic response function)**와 합성하여 생성
   · 이 디자인 매트릭스는 Barch et al. (2013)의 분석을 따름

* **2단계(집단 수준)**: 참가자별로 생성된 **통계 매개변수 맵(statistical parametric maps)**을 집계하여 **집단 수준 분석 수행**

---

### ▶ DCM 전용 GLM 분석 (DCM-specific GLM Analysis)

정준 GLM과 병렬로, **DCM 분석을 위한 별도의 GLM 분석**도 수행되었다. 목적은 다음 두 가지이다:

1. DCM의 수식 (Eq. 1)에 사용되는 **자극 벡터(event vector) x**를 정의하여 **C 행렬(parameter matrix C)** 측정 가능하도록 함
2. **ROI(region of interest) 정의를 위한 F-검정(omnibus F-test)**에 필요한 통계 지표 생성

※ 이 분석은 추론(inference)을 위한 목적이 아니므로, **조건 간 공선성(collinearity)**은 허용됨

---

### ▶ 실험 조건의 모델링 방식

HCP의 대부분 과제는 최소 두 가지 이상의 실험 조건을 포함하며, 조건 간 차이는 일반적으로 다음과 같이 구성된다:

* **기본(baseline) 조건**: 비교적 쉬운 처리 요구
* **중요(critical) 조건**: 인지 부하가 높은, 더 많은 정보 처리와 관련된 조건

Table 1에서 볼드체로 표시된 조건들이 critical 조건임.

이러한 조건들은 **정준 GLM과는 다른 방식으로 DCM에 모델링**된다 (그림 3 참조):

* **정준 GLM**에서는 두 조건을 서로 **독립된 시점**으로 모델링
* **DCM용 GLM**에서는 모든 자극을 **기본(baseline)** 조건으로 포함시키고, 그 중에서 **critical 조건만을 별도로 중첩 모델링**함 (즉, 레이어 방식)

→ 이 layered 방식은 **critical 조건에서의 추가적 정신 처리 과정**을 모델링할 수 있도록 한다

---

### ▶ 조건과 ROI 간의 연결 방식

DCM에서는 각 조건이 특정 ROI에만 영향을 줄 수 있도록 설계할 수 있다.

본 연구에서는 **모든 과제에서 동일한 방식**을 적용하였다:

* **기본(baseline) 조건**은 **지각(perception) ROI**에 영향
* **중요(critical) 조건**은 **작업 기억(working memory, WM) ROI**에만 영향

→ 이 설정은 중요한 조건에서 **더 큰 정신적 노력(mental effort)**이 요구된다는 점에 기반하며, 실제로 모든 GLM 분석에서도 **중요 조건에서 PFC 활성이 더 큼**이 확인되었다 (Barch et al., 2013)

---

## 2.3 관심 영역 정의 (Regions-of-Interest Definition)

각 과제 및 각 참가자마다 관심 영역(region of interest, ROI)을 **객관적으로 정의**하기 위해, 일련의 처리 파이프라인(processing pipeline)이 설계되었다. 이 파이프라인은 다음과 같은 순차적 단계를 따른다:

---

### ▶ 1단계: 이론적 사전 정의 (Macro-level ROI identification)

출발점은 각 **CMC(Common Model of Cognition)** 구성요소를 대규모 신경해부학적 영역과 **이론적으로 선제적으로 연관짓는 것**이었다. 이 연관은 기존 문헌과 대규모 신경인지 아키텍처에서 제시된 기능-구조 매핑(function-to-structure mappings)을 근거로 한다 (예: Anderson, 2007; Borst et al., 2015; Borst & Anderson, 2013; Eliasmith et al., 2012; O’Reilly et al., 2016):

* **작업 기억(working memory, WM)** → 전두-두정 네트워크 (배외측 전전두피질 dorsolateral prefrontal cortex, PFC 및 후두정피질 posterior parietal cortex)
* **장기 기억(long-term memory, LTM)** → 중측두엽, 전측두엽, 상측두엽 영역
* **절차 기억(procedural memory)** → 기저핵(basal ganglia)
* **행동(action)** → 운동 및 전운동 피질(premotor and primary motor cortex)
* **지각(perception)** → 1차 및 2차 감각피질(sensory cortices), 청각피질(auditory cortices), 전체 복측 시각 경로(ventral visual pathway)

(그림 1B 참조)

---

### ▶ 2단계: 집단 수준 정밀화 (Group-level approximation)

이후 각 ROI의 위치를 구체화하기 위해 **두 단계의 점진적 정밀화 과정**을 수행하였다. 먼저, 집단 수준에서 과제 차이(task differences)와 자극 차이(stimulus differences)로 인한 변화를 반영해야 했다. 예컨대,

* **청각 자극 vs 시각 자극** → 서로 다른 감각 영역 활성
* **과제 난이도 또는 유형** → 서로 다른 PFC 영역을 활성화

이를 위해 다음을 수행하였다:

* 각 과제에 대해 **개별적인 집단 수준 GLM 분석(group-level GLM analysis)** 수행
* 각 ROI에 대해 통계적으로 가장 강한 반응을 보이는 **세 영역의 좌표(coord)** 추출:

  1. 시각 영역 (시각피질 및 복측 측두엽)
  2. 배외측 전전두피질
  3. 기저핵 (선조체 striatum 영역으로 제한)

---

### ▶ 3단계: 개인 수준 정밀화 (Individual-level approximation)

다음으로, 위에서 정의한 집단 수준 좌표를 기반으로 **각 참가자의 뇌에서 가장 가까운 활성 좌표(peak activation)**를 탐색함:

* 각 참가자의 개인별 GLM 결과에서 **F-검정(omnibus F-test)** 기반 통계 파라미터 맵을 생성
   → 이는 **모든 조건에 대해 반응을 보이는 voxel을 포착**하기 위함
* 위 F-맵을 이용해, 사전 정의된 각 구성요소의 ROI 근처에서 가장 활성도가 높은 voxel의 **좌표를 자동 탐색**

→ 이 좌표가 **각 참가자별 해당 구성요소의 중심(centroid)**으로 설정됨

이렇게 정의된 좌표는 **시각적으로 검토**되었고, 사전 정의된 해부학적 경계를 벗어난 경우에는 수동으로 조정하였다. 전체 약 1,200개 좌표 중 **단 2개만 (\~0.2%) 수동 수정**이 필요했음.

그림 4는 각 과제에서 수집된 **개인별 ROI 중심 분포**를 시각화한 것이며, 회색 배경은 해당 과제의 **집단 수준 통계 맵**, ‘+’ 마커는 개별 참가자들의 ROI 중심을 나타낸다.

---

### ▶ 최종 ROI 추출 및 신경 활동 표현

각 개인별 ROI 좌표를 중심으로 다음과 같은 절차로 최종 ROI를 정의하였다:

* 좌표를 중심으로 **구형(spherical) ROI** 생성
* 이 구 내부에서 **통계적으로 유의한 활성(p < 0.50)**을 보이는 모든 voxel 포함
* 포함된 voxel들의 시계열로부터 **주성분 분석(principal component analysis, PCA)**를 통해 **가장 큰 주성분 하나를 대표 시계열로 추출**

→ 이렇게 추출된 시계열이 해당 참가자의 해당 ROI의 **신경 활동(time series of neural activity)**을 대표함

---

### ▶ 좌측 반구에만 ROI 설정

모든 ROI는 **좌반구(left hemisphere)**에만 위치하도록 설정하였다. 이는 다음과 같은 이유로 다른 대안(예: 양반구 ROI 설정, 반대편 동형영역 포함)을 배제한 결과이다:

* 양반구 ROI는 포함 voxel 수가 많아져 분산이 증가함
* 동형 영역 포함은 **뇌량(inter-hemispheric)** 연결에 대한 추가 가정을 필요로 함

또한, 모든 과제에서 좌반구 활성도가 우반구보다 강하게 나타났기 때문에, 본 분석 결과는 여전히 **해당 영역에서의 뇌 활동을 대표**한다고 간주할 수 있다.

---

## 2.4 모델 적합 (Model Fitting)

각 ROI(region of interest)에 대해 시계열(time series)이 추출된 후, 다음 절차를 통해 **각 아키텍처별 네트워크 모델**을 구축하였다.

1. 앞서 개인별로 정의된 ROI들을 각기 연결
2. 연결 방식은 각 실험 조건에서 정의한 **아키텍처 구조도(그림 2 참조)**에 따름
    → 예: CMC, 허브-스포크 모델, 계층 모델 등

중요한 점은, 실제 뇌에는 **모든 구성요소 쌍 간의 해부학적 연결(synaptic pathways)**이 존재한다는 점이다.
그러나 본 연구의 네트워크 모델은 **해부학적 세부사항이 아닌**, 각 아키텍처가 가정하는 **기능적으로 필수적인 연결(functionally necessary connections)**만을 반영한 것이다.

---

### ▶ 예측 신경 반응 시뮬레이션

각 네트워크 모델에 대해, 아래 식 (앞서 정의한 DCM 수식, Eq. 1)을 기반으로 **과제 수행 시간 동안의 신경 반응의 시간 흐름(time-course)**을 시뮬레이션하였다:

$$
\frac{dy}{dt} = Ay + Cx
$$

여기서:

* **y**: ROI의 신경 활동 벡터
* **x**: 과제 이벤트 자극 벡터
* **A, C**: ROI 간 연결성 및 자극 효과를 나타내는 파라미터 행렬

---

### ▶ BOLD 신호 생성

시뮬레이션된 신경 활동 y는 **생물학적으로 타당한 신경-혈관 결합 모델(neurovascular coupling model)**을 통해 **예측 BOLD(Blood Oxygenation Level Dependent) 신호**로 변환되었다. 이때 사용된 모델은 **“풍선 모델(balloon model)”**로, 다음을 참고하였다:

* Buxton et al. (1998)
* Friston et al. (2000)

---

### ▶ DCM 파라미터 적합 (Model Parameter Estimation)

각 모델의 전체 DCM(Dynamic Causal Model)은 다음 두 종류의 파라미터를 포함한다:

1. **네트워크 연결 파라미터(network connectivity parameters)**
    → 즉, A 및 C 행렬의 값들
2. **신경-혈관 결합 생리학 파라미터(physiological parameters)**
    → 풍선 모델 내 포함된 변수들

이 파라미터들을 적합하기 위해, **기대-최대화 알고리즘(expectation-maximization procedure)**을 적용하였다 (Friston et al., 2003). 이 알고리즘은 다음을 목표로 한다:

* 시뮬레이션된 BOLD 신호와
* 각 참가자의 실제 측정된 BOLD 시계열

간의 **차이를 최소화(minimize the difference)**하도록 모델을 조정한다.

---

## 3. 결과 (Results)

### 3.1 모델 선택 (Model Selection)

**동적 인과 모델링(Dynamic Causal Modeling, DCM)**은 **베이지안 추론(Bayesian inference)**에 기반한 모델이므로, 주어진 참가자와 과제에 대해 **가장 적합한 모델**을 선택할 수 있는 비교 기준을 제공한다.
이 비교 기준은 바로 **모델 증거(model evidence)**이며, 이는 해당 모델이 주어진 데이터에 대해 관찰될 확률(probability of the data given the model)을 측정한다.

실제로는, 계산의 효율성을 위해 **모델 증거의 로그(log model evidence)**, 즉 **모델의 자유 에너지(variational free energy)**를 사용한다.

---

### ▶ 참가자 수준에서의 모델 비교

각 참가자에 대해, 다음의 7개 모델 모두를 개별적으로 적합(fit)시켰다:

1. **공통 인지 모델(Common Model of Cognition, CMC)**
2. **CMC 변형(CMC*)*\* – CMC에서 perception-action 연결 제거
3. **허브-스포크 모델 (Hub-and-Spoke)** – 중심 허브로 PFC를 설정한 3개 구조
4. **계층 모델 (Hierarchical)** – 세 가지 대체 연결 구조

각 모델에 대해 **개별 참가자별 DCM 분석**을 수행하고, 각 모델의 로그 모델 증거 값을 수집하였다.

---

### ▶ 집단 수준에서의 모델 선택

개별 참가자 수준의 모델 증거를 바탕으로, **집단 수준(group-level)**에서 어느 모델이 가장 가능성 높은지 결정하기 위해 **베이지안 모델 선택(Bayesian model selection)**을 수행하였다 (Rigoux et al., 2014).
이때 사용된 모델은 **랜덤 효과 베이지안 모델(random-effects Bayesian model)**로, 참가자 간 이질성(heterogeneity)을 허용한다.

이 모델은 다음 두 가지 주요 척도를 산출한다:

1. **우세 확률(expected posterior probability)**:
    → 집단 내 임의로 선택된 참가자가 특정 모델을 따를 확률
2. **우월 확률(exceedance probability)**:
    → 해당 모델이 다른 모든 모델보다 우세할 확률

---

### ▶ 결과 요약 (Figure 5)

**그림 5**에는 각 과제별로 모든 모델에 대한 두 척도(우세 확률, 우월 확률)가 제시되어 있다.

* **공통 인지 모델(CMC)**은 모든 과제에서 일관되게 가장 높은 우월 확률을 보였다.
* CMC의 구조적 변형(CMC\*)은 CMC보다 열등한 성능을 보였으며, 특히 일부 과제에서는 모델 비교 기준에 따라 기각되었다.
* 허브-스포크 모델 중 일부는 특정 과제에서 경쟁력이 있었으나, CMC를 능가하지는 못했다.
* 계층 모델들은 전반적으로 낮은 우세 확률과 우월 확률을 보였다.

---

이러한 결과는 다음을 강하게 시사한다:

* 다양한 인지 과제 전반에 걸쳐, **CMC가 신경 활동의 원인적 구조(causal structure)를 가장 잘 설명한다**.
* 특히 **지각(perception)**과 **행동(action)** 간의 직접 연결이 중요한 기제로 작용함을 뒷받침한다.

→ 이는 기존의 순차적 정보처리 모델(sequential information-processing models)이나 단일 허브 모델(single-hub models)보다 더 유연하고 확장성 있는 아키텍처임을 의미한다.

---

### 3.2 모델 적합 품질 (Quality of Model Fit)

**DCM(Dynamic Causal Modeling)**의 핵심 목표 중 하나는, 각 모델이 **fMRI로 측정된 BOLD(Blood Oxygenation Level Dependent) 신호의 시계열(time series)**을 얼마나 잘 설명할 수 있는지를 평가하는 것이다.
이를 위해, 각 모델의 적합 결과와 실제 측정된 뇌 활동 사이의 **상관 계수(correlation coefficient)**를 계산하였다.

---

### ▶ 평가 방법

* 각 참가자에 대해:
   → 실제 ROI 시계열 vs 모델에서 예측된 시계열 간 **피어슨 상관 계수(Pearson correlation coefficient)**를 계산

* 전체 6개 과제에서 200명의 참가자, 각 참가자당 5개 ROI
   → 총 **6,000개 시계열**에 대해 비교 수행

* 이후, 모델 전반에 걸쳐 이들 상관 계수의 **분포(distribution)**를 시각화 (그림 6)

---

### ▶ 주요 결과

* 전반적으로 모든 모델이 실제 BOLD 시계열을 **양의 상관관계로 예측**함
   → 모든 평균 상관 계수(mean r value) > 0

* 대부분의 시계열에서 **상관 계수 r > 0.4**
   → 이는 해당 모델들이 상당히 높은 수준의 설명력을 가진다는 것을 의미

* 특히 **공통 인지 모델(CMC)**은 모든 과제에서 가장 높은 평균 상관 계수를 보였으며, **전 영역에서 0.5를 초과함**

→ 이는 단순히 모델 비교 지표(log model evidence) 상에서 우수할 뿐만 아니라, **실제 데이터 적합 품질에서도 우수함**을 의미

---

### ▶ 그림 6 해설

**Figure 6**은 각 모델의 전체 시계열에 대한 상관 계수 분포를 박스플롯(boxplot)으로 나타낸 것이다.
모든 모델이 대체로 유사한 분포 범위를 보이나, **CMC가 가장 좁고 높은 중심값(median)을 가짐**.

→ 이는 CMC가 **전반적으로 더 일관된 품질로 데이터에 적합**된다는 것을 시사

---

### ▶ 요약

* DCM 기반 모델 중, **CMC는 fMRI 데이터의 시간적 구조를 가장 잘 설명**함
* 단순히 구조적 적합(model evidence) 뿐 아니라, **예측된 시계열의 품질 면에서도 최고 성능**
* 이는 CMC 아키텍처가 **기능적, 구조적 측면 모두에서 인간 두뇌의 인지 처리 메커니즘에 잘 부합**함을 시사

---

### 3.3 모델 일반화 능력 (Generalizability of the Model)

지금까지의 분석은 **각 과제(task)**에 대해 **독립적으로 수행된 것**이다.
하지만 실제 인지 아키텍처(cognitive architecture)로서의 타당성을 확보하려면, **단일한 모델이 여러 과제에 걸쳐 잘 작동해야 한다**.

→ 즉, 모델은 단일 과제에 과적합(overfitting)되지 않고, 다양한 인지 요구 조건에서도 **일관된 설명력을 유지**해야 한다.

---

### ▶ 모델 간 상대적 순위 유지 여부

이를 평가하기 위해, 다음 절차를 수행하였다:

1. **각 과제에 대해**, 참가자별로 7개 모델의 **로그 모델 증거(log model evidence)**를 계산
2. 각 참가자별로 모델의 **상대적 순위를 산정**
3. 이를 **과제 간 비교**하여, 모델 순위가 **일관되게 유지되는지** 확인

---

### ▶ Figure 7 해설

**그림 7**은 각 모델의 **평균 순위(average rank)**를 과제별로 나타낸 것이다.

* **CMC 모델**은 6개 과제 모두에서 **가장 낮은 평균 순위(= 1위)**를 기록
* 다른 모델들은 과제에 따라 등락을 보임
   → 예: CMC\*는 일부 과제에서는 준수한 성능을 보였지만, 전반적으로 불안정한 순위를 가짐
   → 허브-스포크 및 계층 모델도 마찬가지로 불일치적(inconsistent)

---

### ▶ 통계적 분석

이러한 순위 일관성의 통계적 유의성을 검증하기 위해:

* **프리드만 검정(Friedman test)** 수행
   → 비모수(non-parametric) 분산 분석 방법으로, 과제 간 모델 순위의 차이를 평가
* 결과:
   χ²(6) = 124.6, p < 0.001
   → 모델 간 성능에 **유의미한 차이 존재**

이후 사후 분석(post-hoc analysis)을 위해:

* **윌콕슨 부호 순위 검정(Wilcoxon signed-rank tests)**을 통해 CMC와 나머지 모델 간 쌍 비교 수행
* 모든 비교에서 **CMC가 유의미하게 우수**함이 입증됨 (모든 p < 0.001, FDR 보정 적용)

---

### ▶ 요약

* **CMC는 모든 과제에서 가장 일관되게 높은 성능**을 보였으며,
* 이는 단순히 하나의 과제에서 우연히 좋은 성능을 보인 결과가 아니라,
* **인지 기능 전반에 걸쳐 일반화 가능한 신경 구조적 모델임을 강하게 시사**

→ 다시 말해, **CMC는 인간 인지의 공통 기반(common infrastructure)을 반영하는 신경 아키텍처**로 간주할 수 있다.

---

## 4. 논의 (Discussion)

본 연구는 **공통 인지 모델(Common Model of Cognition, CMC)**이 인간 두뇌의 기능적 연결 구조(functional architecture)를 설명하는 데 있어 **다양한 경쟁 모델을 능가한다는 강력한 증거**를 제시하였다. 특히,

* 다양한 인지 과제들(cognitive tasks) 전반에서
* 다양한 연결 구조(connectivity architectures)들과의 비교를 통해
* **원인적 신경 활동(causal neural activity)** 수준에서 분석한 결과,

CMC는 **개별 과제**뿐만 아니라 **과제 전반(task-general)**에서도 일관되게 최고의 성능을 보였다.

---

### ▶ 연구 결과의 핵심 요점

1. **CMC는 유효 연결성(effective connectivity)** 수준에서 가장 설득력 있는 설명을 제공함
2. **모델 적합 품질(model fit quality)** 측면에서도 CMC가 가장 높은 시계열 상관관계를 기록
3. **과제 전반의 일반화 가능성(generalizability)** 측면에서도 CMC는 모든 과제에서 일관되게 가장 낮은 순위(= 최고의 성능)를 유지함

---

### ▶ 기능적 중요성: 지각-행동 직접 연결 (Perception-Action Link)

CMC의 성능을 뒷받침하는 주요 요소 중 하나는 **지각(perception)**과 **행동(action)** 간의 **직접 연결(direct link)**이다.

* 본 연구의 대조 모델 중 다수는 **순차적 처리(sequential processing)**나
   **단일 중심 허브(single central hub)**를 기반으로 한 구조를 채택하였으며,
   → 이는 모든 정보가 중심 처리장소를 통해 흐른다는 전제를 따른다.

* 그러나 **CMC는 지각 정보가 직접적으로 행동 시스템에 영향을 줄 수 있음을 명시적으로 허용**함
   → 이는 생존에 필수적인 **빠른 반응(fast sensorimotor responses)** 및 **자동화된 처리(automated processing)**와 관련 있음
   → 예: 외부 자극에 대한 반사적 반응, 위험 회피 행동 등

이러한 구조는 **인지 부하가 낮은 환경에서의 효율적 처리**를 가능하게 하며,
고차원적인 인지 처리와도 병렬적으로 작동할 수 있는 **유연한 정보 흐름**을 제공한다.

---

### ▶ 신경과학과 인지과학의 통합적 접근 가능성

본 연구는 CMC가 **전통적 인지 아키텍처(cognitive architectures)**로서의 역할뿐 아니라,
**인간 신경계의 기능적 구조(functional neuroarchitecture)**를 설명하는 **신경과학적 모델**로도 유효함을 보여준다.

* 이는 **인지과학(cognitive science)**과 **신경과학(neuroscience)** 간의 오랜 간극을 메우는 데 기여할 수 있음
* 특히 **기계 학습(machine learning)**, **로봇 공학(robotics)**, **인공지능(artificial intelligence)** 분야에서,
   CMC는 인간 유사 지능(human-like intelligence)을 구현하기 위한 **생물학적 타당성을 갖춘(reference-grounded)** 기반 모델이 될 수 있다.

---

### ▶ 한계점 및 향후 과제

1. **단일 참가자별 모델 적합에 따른 불확실성**
    → DCM은 비교적 높은 계산 비용과 제약 조건을 가지므로,
     미세한 연결 패턴을 포착하기 위해 더 고해상도 데이터가 요구될 수 있음

2. **정의된 ROI(region of interest)의 제한성**
    → 본 연구는 총 5개 영역만을 포함했으나,
     보다 정밀한 연결망 분석을 위해서는 **더 많은 뇌 영역**이 포함되어야 할 가능성 있음

3. **정적인 연결성 모델의 한계**
    → 현재 DCM은 고정된 연결 구조(static structure)를 가정하지만,
     실제 인간 두뇌는 **맥락에 따라 동적으로 변화하는 연결성(dynamic reconfiguration)**을 보임
    → 향후 연구는 **시간-가변 DCM(time-varying DCM)** 또는 **적응형 네트워크 모델**로 확장할 필요 있음

---

### ▶ 결론

본 연구는 **공통 인지 모델(CMC)**이 **인간 뇌의 기능적 연결 구조(functional connectivity architecture)**를 설명하는 데 있어,
기존 신경과학 기반 모델들을 **일관되게 능가하는 설득력 있는 후보**임을 실증적으로 제시하였다.
이는 단지 인지과학적 아키텍처의 수준을 넘어서,
**생물학적으로 실현 가능한 인간형 인공지능 모델의 공통 기반(common foundation)**으로 기능할 수 있음을 시사한다.

---
