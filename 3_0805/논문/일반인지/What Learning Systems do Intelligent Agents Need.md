**"What Learning Systems do Intelligent Agents Need? Complementary Learning Systems Theory Updated"**
---

### 초록 (Abstract) 번역

우리는 **보완적 학습 시스템 이론(Complementary Learning Systems theory, CLS theory)**을 업데이트한다. 이 이론은 지능적인 에이전트(intelligent agents)는 **두 개의 학습 시스템**을 가져야 한다고 주장하며, 이는 포유류의 **신피질(neocortex)**과 **해마(hippocampus)**에 구현되어 있다. 첫 번째 시스템은 환경에 대한 구조화된 지식 표현(structured knowledge representations)을 점진적으로 학습하며, 두 번째 시스템은 개별 경험의 구체적인 정보를 빠르게 학습한다.

우리는 이 이론에서 **해마 기억의 재생(replay of hippocampal memories)**의 역할을 확장하며, 재생이 **목표 기반(goal-dependent)**으로 경험의 통계를 가중할 수 있도록 한다는 점을 강조한다. 또한 최근 제기된 이론에 대한 도전들에 응답하며, 해마 흔적의 반복적 활성화(recurrent activation of hippocampal traces)가 일부 일반화(generalization)를 지원할 수 있고, 기존의 지식 구조와 일관되는 정보에 대해서는 **신피질 학습이 빠르게 일어날 수 있음**을 보이며 이론을 확장한다.

마지막으로, 우리는 이 이론이 **인공지능 에이전트 설계**에 주는 시사점을 논의하면서 **신경과학(neuroscience)**과 **기계학습(machine learning)** 간의 연결점을 강조한다.

---

### Complementary Learning Systems

(**보완적 학습 시스템**)

보완적 학습 시스템 이론(Complementary Learning Systems theory, CLS theory)이 제시된 지 20년이 지났다. 이 이론은 **인간의 학습과 기억(human learning and memory)**에 대한 설명을 제공하며, **Marr** 및 기타 학자들의 초기 아이디어에 뿌리를 두고 있다. 이 이론에 따르면, 효과적인 학습은 두 개의 **보완적 시스템(complementary systems)**을 필요로 한다.

하나는 **신피질(neocortex)**에 위치하며, 환경에 대한 **구조화된 지식(structured knowledge)**의 점진적 습득을 담당하고,
다른 하나는 **해마(hippocampus)** 중심에 위치하며, 개별 항목 및 경험에 대한 구체적인 정보를 빠르게 학습할 수 있게 한다.

우리는 먼저 이 이론의 핵심 원칙(core tenets)을 검토하고, 이후 다음의 세 가지 방향에서 이 이론을 업데이트한다.

1. **해마에 저장된 기억의 재생(replay of hippocampal memories)** 역할을 확장한다. 이 메커니즘은 처음에는 신피질에 새로운 정보를 통합하는 과정을 지원하는 역할로 제안되었으나, 이후 **목표 관련(goal-related)** 방식으로 경험 통계를 조작할 수 있도록 하는 등 다양한 기능을 지원할 수 있음이 제시되었다. 즉, 신피질은 환경 통계에만 종속된 학습 기계가 아니라는 것이다.

2. 최근 제기된 두 가지 실험적 도전에 대응하는 업데이트를 설명한다:
   (i) **해마가 초기 이론에서 상정한 수준을 넘어서 일부 일반화(generalization)**를 지원한다는 증거 \[4–6],
   (ii) **새로운 정보가 기존 지식과 일치하는 경우**, 해당 정보가 신피질에 통합되기까지의 시간이 초기 예상보다 훨씬 짧을 수 있다는 증거 \[7,8].

3. 마지막으로, 우리는 CLS 이론의 핵심 원리와 **최근 기계학습(machine learning)** 분야의 주요 주제들 간의 연결을 조명한다. 여기에는 **해마와 유사한 기능을 수행하는 메모리 모듈(memory modules)**을 포함하는 **신경망 구조(neural network architectures)**가 포함된다.

아직 해결되지 않은 여러 문제들이 남아 있음에도(‘Outstanding Questions’ 참조), 이 이론에 대한 확장, 도전에 대한 응답, 기계학습과의 통합은 이 이론을 **최신 과학 발전과의 정합성** 속에 놓이게 하며, 향후 연구를 위한 출발점으로 작용한다.

---

### 최근 동향 (Trends)

* **경험의 집합(ensembles of experiences)** 속에서 구조를 발견하는 능력은 **신피질 생물학적 신경망(biological neural networks in neocortex)**과 **현대 인공 신경망(contemporary artificial neural networks)** 모두에서 **교차(interleaved)** 학습 과정에 의존한다.

* 최근 연구들은, 일단 **구조화된 지식(structured knowledge)**이 이러한 네트워크에 획득되면, **새로운 일관된 정보(new consistent information)**는 빠르게 통합될 수 있음을 보여준다.

* **자연(natural)** 및 **인공 학습 시스템(artificial learning systems)** 모두는 **개별 경험(specific experiences)**을 저장하는 **두 번째 시스템**에서 이익을 얻으며, 포유류에서는 이것이 **해마(hippocampus)** 중심에 존재한다.

* 이 시스템으로부터의 경험 재생(replay of experiences)은 **교차 학습(interleaved learning)**을 지원하며, **보상(reward)**이나 **새로움(novelty)**에 의해 조절될 수 있어, 환경의 일반 통계를 **에이전트의 목표(goals of the agent)**에 맞게 재조정할 수 있다.

* **인스턴스 기반 시스템(instance-based system)** 내에서의 **다수 기억들의 반복적 활성화(recurrent activation of multiple memories)**는 경험 간의 연결(link)을 발견하는 데 사용될 수 있으며, 이는 **일반화(generalization)**와 **기억 기반 추론(memory-based reasoning)**을 지원한다.

---

### CLS 이론 요약 (Summary of the Theory)

**CLS 이론 \[1]**은 뇌에서의 학습 조직화(organization of learning)에 대한 특징화 틀을 제공한다 (Figure 1, **핵심 그림(Key Figure)** 참조). 이 이론은 David Marr의 초기 아이디어에서 출발하여, **해마(hippocampus)**와 **신피질(neocortex)**의 계산적 기능과 특성에 대한 종합을 제시한다. 이 구성은 다양한 실험적 자료들을 설명해줄 뿐만 아니라, **지능적 에이전트가 직면하는 학습 과제에 대한 합리적 관점(rational perspectives)**과도 잘 들어맞는다.

---

### 신피질의 구조화된 지식 표현 시스템

(**Structured Knowledge Representation System in Neocortex**)

이 이론의 중심 명제(central tenet)는 **신피질(neocortex)**이 **구조화된 지식 표현(structured knowledge representation)**을 저장하고 있으며, 이는 신피질 내 뉴런들 간 연결(connection) 속에 저장된다는 것이다.
이러한 주장은 다음의 관찰에서 비롯된다: **다층 신경망(multi-layered neural networks)**은 **출력 오류(output error)**를 최소화하도록 **연결 가중치(connection weights)**를 조정하는 방식으로 훈련되면서, 점차적으로 구조를 학습한다(Figure 2).

초기의 대표적인 예시는 **단어의 철자(spelling)**와 해당 **소리(sound)**에 반복적으로, 교차적으로 노출된 후, 영어 단어를 **소리 내어 읽는 방법을 학습(read aloud)**한 신경망들에서 제공되었다 \[11–13].
이러한 신경망은 **환경의 통계(statistics of the environment)**에 의해 형성된 연결 가중치들을 통해 **구조화된 지식 표현(structured knowledge representation)**을 점차 습득하였으며,
이는 새로운 예시(novel examples)에 일반화되며 동시에 해당 영역에서 자주 발생하는 **비정형 항목(atypical items)**에 대한 수행 역시 가능하게 했다 \[1,14,15].

이러한 표현은 **항목 기반(item-based)** 혹은 **비모수적(non-parametric)**이라기보다는 **모수적(parametric)**이라 설명된다.
그 이유는, 이 연결 가중치들이 개별 항목 각각에 대한 기억을 저장한다기보다는, **전체 도메인(domain)** (예: 전체 단어 집합의 철자와 발음)에 최적화된 **모수 집합(parameter set)**이라 볼 수 있기 때문이다.

이 이론에 따르면, 이러한 **신경망(neural networks)**은 지각(perception), 언어(language), 의미 지식 표현(semantic knowledge representation), 숙련된 행동(skilled action) 등과 같이 다양한 영역에서 **획득된 인지 능력(acquired cognitive abilities)**의 기초가 된다.
이러한 관점은 **Marr**의 원래 제안 \[9]에 대한 확장으로 볼 수 있으며, 그는 각 **피질 뉴런(cortical neuron)**이 특정 범주(category)에 대한 통계를 학습한다고 주장했다.

---

**CLS 이론**은 이러한 **모수적 시스템(parametric system)**에서의 학습은 필연적으로 **느릴 수밖에 없다**고 주장한다. 그 이유는 크게 두 가지이다:

1. **각 경험은 환경으로부터 추출된 단일 샘플(single sample)**에 불과하다.
   이러한 조건에서는 **작은 학습률(small learning rate)**을 사용하는 것이 **모집단 통계(population statistics)**의 더 정확한 추정치를 얻는 데 유리하다. 이는 더 많은 샘플에 걸쳐 정보를 효과적으로 누적(aggregate)하기 때문이다 \[1].

2. 각 연결(connection)의 최적 조정은 **다른 모든 연결의 값(values)**에 의존한다.
   즉, 연결들의 집합(ensemble)이 경험을 통해 구조화되기 전에는, **가중치 변경을 위한 신호(signals)**는 **약하고 노이즈(noisy)**가 많아 초기 학습이 느려진다.

이러한 문제는 **심층 신경망 구조(deep neural network architectures)** – 즉, 다층 구조를 가지며 최근 기계학습에서 큰 성공을 거두고 있는 모델들 \[16] – 에서 특히 중요한 것으로 나타났다.

---

이러한 **깊이(depth)**가 제공하는 이점, 즉 **점점 더 복잡하고 추상적인 매핑(abstract mappings)**을 학습할 수 있는 능력 \[16]은, 반대로 **깊은 신경망에서의 가중치 간 강한 상호의존성(strong interdependencies among connection weights)**이라는 대가를 수반한다 \[19,20].
따라서 이러한 네트워크는 **도메인 통계(domain statistics)**를 담은 **훈련 예시(training examples)**들의 집합을 대상으로 **광범위하고 반복적이며 교차적인 노출(repeated and interleaved exposure)**을 통해 점진적으로 학습된다.

---

### 신피질 시스템의 한계점

(Disadvantages of the Neocortical System Alone)

**구조화된 모수적 표현(structured parametric representations)**을 사용하는 시스템에는 분명한 장점이 존재하지만, 이 시스템만으로는 다음과 같은 **두 가지 심각한 한계(two drastic limitations)**가 발생한다 \[1].

1. **개별 경험(individual experience)의 내용**을 기반으로 행동을 결정할 수 있어야 한다.
   예를 들어, 사자가 출몰하는 **급박하고 위험한 사건(life-threatening situation)**을 한 번 경험했다면, 더 이상의 반복적인 노출 없이도 **그 장소를 피하는 행동**을 학습하는 것이 유리하다.

2. 다층 신경망(multi-layer network)에서 **새로운 정보를 반영하기 위해 연결 가중치(connection weights)를 빠르게 조정**하는 경우, **기존 지식의 표현(existing knowledge representation)**을 심각하게 훼손할 수 있다.
   이 현상은 **치명적 간섭(catastrophic interference)**으로 알려져 있으며 \[1,21–23], 이는 **안정성–가소성 딜레마(stability–plasticity dilemma)**와도 관련된다 \[24].

예를 들어, 위험한 사자에 대한 정보를 빠르게 학습하려고 새로운 항목을 다층 신경망에 삽입하기 위해 **가중치를 크게 조정**하게 되면, 이미 학습된 **위협적이지 않은 동물들**에 대한 지식이 손상될 수 있다.

---

### 해마 시스템의 인스턴스 기반 표현

(**Instance-Based Representation in the Hippocampal System**)

다행히도, 두 가지 문제를 모두 해결할 수 있는 **두 번째 보완적 학습 시스템(complementary learning system)**이 존재한다.
이 시스템은 **개별 항목이나 경험(individual items or experiences)**에 대한 정보를 **빠르고 구체적으로 저장**할 수 있는 능력을 제공한다.
예를 들어, 사자를 마주쳤던 장소(물웅덩이)에 대한 세부 정보와 그 사자의 특징은 모두 이 시스템에 저장된다.

**Marr** 및 후속 이론들 \[25–27]을 바탕으로, **CLS 이론**은 **해마(hippocampus)**와 그와 연관된 **내측측두엽 구조들(medial temporal lobe, MTL)**이
이러한 개별 정보(item-specific information)의 초기 저장(initial storage)을 지원한다고 제안한다 (Figure 1 참조).

이 제안은 **특정 항목에 대한 인식 기억(recognition memory)**과, 동일한 사건이나 경험 내에서 항목들의 **문맥(context)** 및 **공동 발생(co-occurrence)**에 대한 민감성에 있어
**해마의 역할을 모델링한 연구들(models)**에서도 관찰된다 \[28–36].

---

CLS 이론에서, 해마의 **치아이랑(dentate gyrus, DG)** 및 **CA3 아구역(subregion)**은 **빠른 학습 시스템(fast learning system)**의 핵심을 이룬다 (Boxes 2–4 참조).
DG는 서로 유사한 경험들 간에도 **각 경험마다 뚜렷한 신경 활성 패턴(distinct neural activity pattern)**을 **CA3**에서 선택해내는 데 핵심적인 역할을 한다 \[25–27,37,38].
이러한 과정은 **패턴 분리(pattern separation)**라고 불린다.

해당 경험의 **활성 패턴(activity pattern)**을 안정화시키기 위해, DG 및 CA3 뉴런들 사이의 연결 강도(strength of connections)는 증가하게 되고,
이는 **부분 단서(partial cue)**로부터 **기억의 재활성화(reactivation)**를 가능하게 한다.

예를 들어, 사자를 마주쳤던 물웅덩이 장소라는 일부 정보만 제공되어도, 이 경험 전체(사자와의 조우)가 **재구성(reconstruct)**될 수 있게 된다.
이 과정을 **패턴 완성(pattern completion)**이라 부른다.

이후, **해마에서 신피질로의 귀환 연결(return connections)**은 적절한 행동(예: 해당 장소 회피)을 가능하게 한다.

---

다만, 해마 시스템 단독으로도 **충분하지 않다(insufficient)**는 점에 유의해야 한다.
그 이유는 다음과 같다:

* **저장 용량(capacity limitations)**이 제한적이며 \[26]
* **일반화 능력(generalization ability)**도 제한되어 있기 때문이다.

---

### 해마의 패턴 분리와 일반화의 한계

(How Pattern Separation in the Hippocampus Limits Generalization)

**유사한 경험들(similar experiences)**에 대해 **패턴 분리된 해마 코드(pattern-separated hippocampal codes)**를 사용하는 것은
일정한 목적에서는 유리할 수 있지만, 동시에 **효율성(efficiency)**과 **일반화 능력(generalization)** 측면에서 **비용(cost)**이 따른다.

예를 들어, **모수적 신피질 시스템(parametric neocortical system)**에서는 **상대적으로 밀집된 유사성 기반 코딩(dense similarity-based coding scheme)**이 작동하는 반면,
해마에서는 서로 비슷한 사건이라도 **각각을 완전히 분리된 코드로 처리**한다.
이로 인해, **공통 구조(shared structure)**를 무시하게 되며, 이는 일반화 및 학습 자원의 효율적 사용에 불리하게 작용한다.

---

### 신피질과 해마의 대표성 차이

(Differences in Representational Properties between Neocortex and Hippocampus)

연구 결과들은 일반적으로, **신피질에서의 활동 패턴(neocortical activity patterns)**이 해마에 비해 다음과 같은 경향이 있음을 보여준다:

* **스파스성(sparsity)**이 낮고
* **유사성 기반 중첩(similarity-based overlap)**이 더 크다 \[17,40,41,43–47] (Boxes 4, 5 참조)

다만, 이러한 **스파스성(sparsity)**과 **중첩(overlap)**의 정도는 **해마와 신피질의 아구역(subregions)**마다 다를 수 있다.
일부 연구에서는 이런 차이를 바탕으로 **다른 이론(other theories)**을 지지한다고 해석했지만 \[48],
이러한 결과는 **CLS 이론과도 충분히 정합적**이며, 오히려 오랫동안 **각 해마 아구역의 역할 분화**를 설명하는 데 사용되어 왔다 (Boxes 2–4).

비슷하게, **학습률(learning rates)**도 해마 내의 아구역들 사이에서 차이가 존재하며 (Box 2),
신피질 영역 간에도 학습률이 서로 다를 가능성이 제기된다 (Box 5).

---

### 과업 수행에서의 두 시스템의 공동 기여

(**Joint Contribution to Task Performance**)

**CLS 이론**에 따르면, **해마 시스템(hippocampal system)**과 **신피질 시스템(neocortical system)**은
많은 과업(tasks)과 다양한 유형의 기억(memories) 수행에서 **함께 기여(jointly contribute)**한다.

이러한 관점은 전통적으로 다음과 같이 구분되어 온 다양한 기억 유형에도 적용된다:

* **일화 기억(episodic memory)**: 특정한 하나의 경험 내 요소들에 대한 기억
* **의미 기억(semantic memory)**: 사물의 특성 같은 사실(facts)에 대한 지식
* **암묵 기억(implicit memory)**: 과거 경험에 의한 수행 향상, 단 그 경험에 대한 **의식적 회상(explicit recollection)** 없이 일어나는 것

CLS 이론에서는 이러한 **기억 유형(memory types)**과 과업(task)은 **연속선(continuum)** 상에 놓이며,
과업, 자극 항목(item), 기타 조건들에 따라 두 시스템의 **상대적 기여 정도(degree of dependence)**가 달라진다고 본다.

---

예를 들어, **쌍연합 학습(task of learning paired associates)**을 생각해보자.
이는 강한, 약한, 또는 명확한 관련이 없는 항목쌍(예: ‘개–고양이’, ‘무거운–여행가방’, ‘도시–호랑이’)들을 포함할 수 있다.

첫 번째 단어를 단서로 제시하고 두 번째 단어를 회상하도록 할 때,
**해마 손상 환자(hippocampal patients)**는 정상인에 비해 성능이 낮지만,
두 그룹 모두 **기존 연관이 강한 항목쌍에 대해서는 더 나은 수행**을 보인다 \[49].

이러한 결과는 다음과 같은 모델 \[50]로 설명할 수 있다 (K. Kwok, PhD Thesis, Carnegie Mellon University, 2003):

* **신피질 네트워크**는 기존의 **배경적 연합 지식(background associative knowledge)**을 담당하고,
* **해마 네트워크**는 학습 중 각 항목쌍과 그 **학습 문맥(learning context)** 간의 연합을 담당한다.

---

### Box 2. 내측 측두엽(MTL)의 아구역별 기능적 역할

(**Functional Roles of Subregions of the Medial Temporal Lobes**)

**CLS 이론(CLS framework)** 하에서의 연구 \[27,116,141]는
**MTL(내측 측두엽, Medial Temporal Lobe)**의 해부학적(anatomical) 및 생리학적(physiological) 특성과,
기존의 계산적 통찰(computational insights) \[9,25,26]에 기반하여
각 하위 구조(subregion)들이 수행하는 연산을 특징화한다.

---

#### ● 해마계 입력을 담당하는 내후각피질 (Entorhinal Cortex, ERC)

경험이 발생할 때, **신피질로부터의 입력(neocortical input)**은 **ERC(entorhinal cortex)** 내에서
해당 경험을 구성하는 패턴들에 대한 일종의 **압축된 표현(compressed description)**을 생성한다.
→ (도해에서 파란색으로 나타난 ERC 뉴런들이 이를 나타냄)

ERC 뉴런은 다음의 세 아구역으로 투사(projection)를 보낸다:

* 치아이랑 (**Dentate Gyrus, DG**)
* CA1
* CA3

---

#### ● 패턴 선택 및 패턴 분리 (Pattern Selection and Pattern Separation)

새로운 ERC 패턴은,
아직 **기억 저장에 사용되지 않은 DG 뉴런들(uncommitted DG neurons)**의 일부를 활성화하며 (도해에서 빨간색),
이들은 다시 CA3로 강력한 **'기폭 시냅스(detonator synapse)'**를 통해 **무작위 하위 집합의 CA3 뉴런**을 선택한다.
→ 이로써 해당 경험에 대한 새로운 CA3 패턴이, 다른 경험들과 최대한 **구별되도록(distinct)** 형성된다.
→ 이 과정은 **기존의 유사한 경험들과의 간섭(interference)**을 줄이는 데 핵심적인 역할을 한다.
(Box 3, 4에서 구체적 설명)

---

#### ● 패턴 완성 (Pattern Completion)

경험 중, 활성화된 CA3 뉴런 간의 **재귀 연결(recurrent connections)**이 강화되어,
후에 같은 뉴런 일부만 활성화되더라도 나머지 뉴런들까지 재활성화된다.
→ 이것이 **패턴 완성(pattern completion)**이며, 부분 단서로 전체 기억을 복원할 수 있게 한다.

또한 ERC에서 CA3로의 **직접 연결(direct connections)**도 강화되어,
이후 **DG 경유 없이도** ERC 입력만으로 **CA3 패턴을 직접 재활성화**할 수 있다 (Box 3 참조).

---

#### ● ERC 및 신피질 내에서의 패턴 재생 (Pattern Reinstatement in ERC and Neocortex)

CA1과 ERC 간의 연결은 **상대적으로 천천히 변화(slowly changing)**하며,
→ CA1–ERC 간의 **안정적인 대응 관계(stable correspondence)**를 유지한다.

기억 인코딩 중, 활성화된 **CA3 → CA1 연결**이 강화되며,
→ 나중에 CA3가 다시 활성화되면 대응하는 CA1 패턴이 재활성화된다.
→ 이는 다시 ERC 패턴을 재생시키고,
→ **ERC와 신피질 사이의 안정된 연결**을 통해 해당 패턴이 **신피질로 전파(propagation)**된다.

---

이러한 **CA1–ERC 간 양방향 연결**과 **ERC–신피질 간 양방향 연결**은 다음을 가능하게 한다:

* **CA1에서의 가역적 표현 형성 및 디코딩(invertible representations and decoding)**
* **재귀적 계산(recurrent computations)**

CLS 이론에서, 해마가 **기억에 장기간 관여(long-term involvement)**한다는 점을 고려할 때,
이러한 연결들이 **빠르게 변화하지 않아야 한다**.
→ 그렇지 않으면, **해마에서 신피질로의 기억 재생이 어렵게 된다** \[61].

---

도해 설명:
도해는 CA3, CA1, DG, ERC, 신피질(Neocortex)의 연결 구조와 정보 흐름을 보여준다.

* 빨간색 선: **시냅스 가소성이 높은 연결(highly-plastic synapses)**
* 회색 선: **가소성이 낮거나 안정적인 연결(less-plastic or stable projections)**
* 점선: **ERC/신피질 → 해마로의 피드백 연결(feedback connections)**
  → 이는 REMERGE 모델(뒤에 소개됨)에서 제안된 구성이다.

---

### 해마 기억의 재생과 교차 학습

(**Replay of Hippocampal Memories and Interleaved Learning**)

이제 우리는 **CLS 이론**의 핵심 초점 중 두 가지인
① **해마 기억의 재생(replay of hippocampal memories)**과
② **교차 학습(interleaved learning)**에 대해 논의하고자 한다.

이 이론에 따르면, **하나의 사건(event)을 학습하는 동안 형성된 해마 표현(hippocampal representation)**은
그 사건에 대한 지식을 **점진적으로 신피질 지식 구조(neocortical knowledge structures)**에 통합할 수 있는 수단이 된다.

이것은 다음의 경우에 가능하다:
→ 해마 표현이 **새로운 경험의 내용(contents of the new experience)**을
**신피질(neocortex)**로 **재활성화 또는 재생(replay)**할 수 있고,
이것이 **다른 경험들과의 교차적 노출(interleaved exposure)**과 결합되는 경우 \[1].

이러한 방식으로, 새 경험은 **신피질 학습 시스템의 연결(connection weights)**을 결정하는
**경험 데이터베이스(database of experiences)**의 일부가 된다 \[51–53].

---

그렇다면, 어떤 기억들이 새로운 경험과 함께 교차적으로 선택되어 재생될까?
→ 이 문제는 여전히 **열린 질문(open question)**이다.

가장 단순한 가능성은 다음과 같다:
→ 해마는 최근의 새로운 경험들을 **다른 최근 경험들과 함께** 재생할 수 있다.
→ 즉, 해마에 여전히 저장되어 있는 **모든 최근 기억들과의 교차적 재생**이다.

---

또 다른 가능성은 다음과 같다:

* 새로운 경험이 해마 내에서 **관련된 다른 경험들을 활성화**시키고
* **재귀적 메커니즘(recurrent mechanism)**을 통해 **해당 관련 기억들과 교차적으로 학습**되는 방식이다.
  → 이는 **REMERGE 모델 \[5]**에서 구현된 방식이다 (뒤에서 설명됨).

또 다른 대안적 관점은 다음과 같다:

* 실제로는 **이전 경험의 충실한 재생(faithful replay)**이 일어나지 않고,
* 오히려 해마 재생은 최근 경험과 함께
  **신피질 네트워크 내의 구조화된 지식(structured knowledge)**에 **일치하는 패턴들**을
  **활성화**하는 과정일 수도 있다.
  → 예: \[23, 54–56]

---

요약하자면, **CLS 이론**이 제안하는 **이중 시스템 구조(dual-system architecture)**는
각 시스템이 가진 상보적 특성(complementary properties)을 **효과적으로 활용**한다.

* 새로운 정보는 **해마에 빠르게 저장(rapid storage in hippocampus)**되고
* 이후 **신피질 표현(neocortical representations)**에 **서서히 통합(gradually integrated)**된다.

이 과정은 때때로 **시스템 수준 통합(systems-level consolidation)**이라 불린다 \[51].

→ CLS 이론에 따르면, 이는
**새로운 정보에 대한 재생(replay of the new information)**이
**다른 활동들과 교차되어(interleaved with other activity)** 일어날 때,
기존 지식에 대한 **방해(disruption)** 없이 신피질 학습이 진행되면서 이루어진다.

---

### 해마 재생의 실증적 증거

(**Empirical Evidence of Replay**)

**CLS 이론**에서 재생(replay)은 핵심적인 요소이므로,
우리는 **재생 현상이 실제로 발생한다는 주요 실험적 증거(empirical evidence)**를 강조하고자 한다.

이러한 데이터는 주로 **설치류(rodents)**를 대상으로 한 연구에서 도출되었으며,
이는 동물들이 **비활동 상태(inactivity)**—예: **수면(sleep)** 또는 **휴식(rest)**—에 있을 때 기록되었다.

이러한 상태에서, 해마 뉴런들은
**활동 상태(active states)**에서와는 뚜렷하게 구분되는
**불규칙한 대규모 활동 패턴(large irregular activity, LIA)**을 나타낸다 \[2,3].

---

LIA 상태에서는 다음과 같은 생리학적 현상이 발생한다:

* 해마의 **CA3 영역(hippocampal area CA3)**에서 시작된다고 추정되는
* **동기화된 발화(synchronous discharges)**가 발생하며
* 이는 **CA1 영역**으로 전파되어
* **샤프-웨이브 리플(sharp-wave ripples, SWRs)**이라 불리는 현상을 유도한다.

→ **SWRs**는 **실제 경험 동안 발생한 활동 패턴(activity patterns)**의
**재활성화(replay)**를 반영하는 것으로 간주된다.

→ 구체적으로는, **장소 세포(place cells)**라고 불리는 뉴런들이
해당 동물이 특정 위치에 있을 때 발화했던 순서대로
**재생성(sequential firing)**되는 것이 관찰된다 \[2,3,57–59].

---

또한 이 재생은:

* 실제 경험 중의 시간보다 약 **20배 압축된 속도(time-compressed by a factor of \~20)**로 발생하며,
* 이로 인해 시간적으로 떨어져 있던 뉴런들의 **스파이크(spikes)**가
* **시냅스 가소성(synaptic plasticity)**을 촉진할 수 있는
  **시간 창(time-window)** 안에 함께 묶이게 된다.

이러한 메커니즘은:

* **해마 내부**, 그리고
* **해마–신피질 간 경로** 모두에서
* **시냅스 강화**를 유도하며,
* 단일 경험(single experience)이 **하나의 수면 주기 동안 여러 차례 반복 재생될 수 있도록** 한다 \[1–3,58,60,61].

---

CLS 이론이 예측한 바와 같이,
**해마의 SWRs**는 **신피질 활동 상태(neocortical activity states)**와 동기화(synchronization)된다 \[62,63].

또한, **해마 내 특정 장소 시퀀스(place sequences)**의 재생은
**내후각피질(entorhinal cortex)** 깊은 층의 **그리드 세포(grid cells)**에서도
**유사한 패턴의 재생**과 연관되어 있음이 밝혀졌다 \[64].
→ 이 층은 해마 출력(output)을 받는 부위이다.

이러한 재생은 심지어 **더 먼 신피질 영역(distal neocortical regions)**에서도 관찰된다 \[65].

---

최근 한 연구에서는 다음과 같은 결과도 발견되었다:

* **서파 수면(slow-wave sleep, SWS)** 동안
* 해마와 **복측 선조체(ventral striatum)**의 뉴런들이
* **동기적으로 재활성화(coordinated reactivation)**되는 현상이 나타났다.

→ 특히, **해마 위치 특이적 재생(location-specific hippocampal replay)**이
**보상 관련 선조체 뉴런(reward-sensitive striatal neurons)**의 활동보다 **먼저 발생**했다 \[66].

---

이러한 재생의 **인과적 역할(causal role)**을 지지하는 연구도 있다.
예를 들어, **해마에서의 리플 활동(ripples in the hippocampus)**을 인위적으로 **차단(disruption)**하면
**시스템 수준 통합(systems-level consolidation)**이 명확히 저해된다.

→ 이 효과는 설치류 실험에서 확인되었으며 \[67–69],
→ 재생이 실제로 **장기 기억 통합(long-term memory consolidation)**에 핵심적임을 보여준다.

---

### 재생의 추가적 기능들

(**Additional Roles of Replay**)

최근 연구들은 **재생(replay)**이 단순히 **시스템 수준 통합(systems-level consolidation)**을 넘어서,
훨씬 **더 다양한 기능들**을 수행할 수 있음을 보여주고 있다.
→ 이러한 기능들은 **LIA 상태(large irregular activity)**뿐만 아니라
**세타 상태(theta states)**에서도 발생한다 \[3,70,71].

---

구체적으로, 해마 재생은 다음과 같은 특징들을 가진다:

1. **비국소적 특성(Non-local nature)**:

   * 재생은 종종 동물의 **현재 위치(current position)**와는 **무관한 장소**에 해당하는
     **장소 세포(place cell)**들의 활동에서 **시작될 수 있다** \[3].

2. **새로운 지름길 경로의 생성(Shortcut path generation)**:

   * 과거 경험의 일부 궤적(trajectories)들을 **이어 붙여(stitching together)**
     **새로운 경로를 구성**할 수 있다 \[72,73].

3. **목표 지향 행동 중의 계획 지원(Planning during goal-directed behavior)**:

   * **목표 지향적 행동(goal-directed behavior)** 중,
     **미래 경로를 미리 살펴보는(look-ahead)** 방식으로 **온라인 계획**을 지원할 수 있다 \[70,74].

4. **한 번도 방문하지 않은 장소의 경로 재생(Path replay through seen-but-not-visited regions)**:

   * 이전에 **눈으로만 본 장소**(but never physically visited)를 포함한 경로를
     **재생할 수 있다** \[75].

5. **보상 위치 중심의 편향된 재생(Reward-biased replay)**:

   * 해마 재생은 환경 내에서 **보상이 주어진 장소들(rewarded locations)**을
     더 자주 재생하는 **편향(bias)**을 보인다 \[76].

---

이러한 증거들은 다음과 같은 결론을 시사한다:
→ **해마 재생(hippocampal replay)**은 단순한 기억 재현을 넘어서
**환경의 표현(representations of the environment)**을

* **생성(create)**하고
* **업데이트(update)**하며
* **활용(deploy)**하는 데까지 이르는 **광범위한 역할(pervasive role)**을 수행한다 \[3].

---

이러한 기능들은 다음과 같은 인지적 관점과도 잘 부합한다:

* **미래 계획(prospection)**에서 해마의 역할 \[77]
* **상상(imagination)** 능력에서의 해마의 기여 \[78,79]
* **통계적 요약(summary statistics)** 기반의 일반적 통제보다
  **개별 에피소드 기반의 통제(episodic control)**가 더 유리할 수 있는 경우들에 대한 설명
  → 예: 환경에서 **충분한 경험이 누적되지 않았을 때(relatively little experience)** \[80]

---

### 해마가 환경 통계를 우회하는 역할

(**Proposed Role for the Hippocampus in Circumventing the Statistics of the Environment**)

앞서 보았듯이, **LIA 상태(large irregular activity)** 동안의 **해마 활동(hippocampal activity)**은
단순히 **최근 경험의 충실한 재생(faithful replay of recent experiences)**을 반영하는 것만은 아니다.

오히려, 최근 축적된 증거들은 **재생 과정이 다음과 같이 편향(biased)**되어 있음을 보여준다:
→ **보상이 주어진 사건들(rewarding events)**을 **우선적으로 재생**한다 \[59,76].

---

이를 바탕으로 우리는 다음과 같은 **더 확장된 가설(broader hypothesis)**을 제안한다:

> 해마는 환경의 일반적인 통계(general statistics of the environment)에 단순히 종속되지 않고,
> **개별 경험들(individual experiences)**을 **재가중(reweighting)**함으로써 이를 **우회(circumvent)**할 수 있다.

즉, 통계적으로는 **비일반적이지만 의미 있는 사건(statistically rare but significant events)**은
다음과 같은 방식으로 **특별 대우(privileged status)**를 받게 된다:

* **우선 저장(preferential storage)**
* **우선 안정화(preferential stabilization)**
* **우선 재생(preferential replay)**

이러한 과정은 **신피질 학습(neocortical learning)**에도 직접 영향을 미치게 된다.

---

우리는 이러한 **해마의 재가중 기능(reweighting function)**이
다음과 같은 상황에서 특히 중요하다고 본다:

* **기억 용량(memory capacity)**이 제한된 상황
* **환경 탐색이 불완전(incomplete exploration)**한 상황

이러한 재가중 기능은 **생물학적 및 인공지능적 에이전트 모두에서**,
그들의 기억 체계를 **더 풍부하게(enrich)** 만들어주는 역할을 할 수 있다.

이러한 관점은 다음과 같은 이론적 프레임워크와도 연결된다:

* **기억 시스템(memory systems)**은 단순히 환경 통계를 반영하기보다는
* **유기체의 목표(goals of the organism)**에 맞게 최적화되어 있다는 **합리적 관점(rational accounts)** \[81]

---

### 개별 경험의 중요도에 영향을 미치는 요인과 해마의 역할

(**Factors Affecting the Significance of Individual Experiences and the Role of the Hippocampus**)

**개별 경험(individual experiences)**의 **의미(significance)**를 결정하는 데 영향을 줄 수 있는 요인은 매우 다양하다 \[82,83]. 예를 들어, 그 경험은 다음과 같은 특성을 가질 수 있다:

* **놀라움(surprising)** 또는 **새로움(novelty)**
* **보상 가치(reward value)**가 매우 높거나 낮음
* 또는 **정보적 가치(informational content)**가 높음
  → 예: 주어진 상태(state)에서 어떤 행동이 최선인지에 대한 **불확실성을 줄이는 데 도움**을 줄 때

---

**해마(hippocampus)**는 다음 두 가지 종류의 입력을 수용할 수 있는 **이상적인 위치**에 있다:

1. **다양한 감각 양식(multimodal sensory information)**에서 **고차원적으로 처리된 정보(highly processed information)**
2. **이러한 의미 요인들(significance factors)**에 의해 유발된 **신경조절성 신호(neuromodulatory signals)** \[84]

이를 통해 해마는 **개별 에피소드별로 그 중요도를 판단하고 조절할 수 있는 위치**에 있게 된다.

---

실제로 최근 연구들은 다음과 같은 **분자 수준의 기전(molecular mechanisms)**을 제시하고 있다:

* **기억 안정화(memory stabilization)**를 지원하는 분자 메커니즘들 \[83,86–88]
* **해마로 투사(projection)**되는 **특정 신경조절 경로(specific neuromodulatory pathways)**
  → 이러한 메커니즘들은 경험 이후에 발생하는 사건들에 따라 **기억 흔적의 지속성(persistence of memory traces)**을 조절할 수 있게 한다.

즉, 특정 에피소드의 중요도가 **사후적으로 증가(retrospectively enhanced)**되었을 경우,
그 기억이 **더 잘 유지되고, 더 자주 재생되도록 유도**될 수 있다 \[83,89].

→ 이로 인해 **재생의 확률(probability of replay)**도 영향을 받게 된다.

---

이러한 **재가중 능력(reweighting capability)**의 중요성은 다음 예시에서 특히 잘 드러난다:

> 아이가 점진적으로 세상에 대한 개념 지식을 습득하는 중이라 하자.
> 예를 들어, "개(dog)는 일반적으로 친근하다(friendly)"는 사실을 여러 경험을 통해 서서히 학습한다.
> 그런데 어느 날, 매우 공격적인 개를 마주치는 일이 발생한다면?

이 사건은:

* **놀랍고(surprising)**
* **새롭고(novel)**
* **감정적으로 강렬한(emotionally charged)** 사건이 될 것이다.

이러한 **의미 있는 단일 경험(significant one-shot experience)**은 다음 두 가지 측면에서 중요하다:

1. **해마에 빠르게 저장되는 것(rapid storage in hippocampus)**
2. **기존의 신피질 지식 구조(neocortical knowledge structures)**에 **적절히 반영(updating)**되는 것

---

**CLS 이론의 초기 버전**은 (1)의 측면, 즉 **단발적 사건의 초기 저장(initial storage of one-shot experiences)**에 해마가 핵심 역할을 한다고 강조하였다.

하지만 이 절에서는, 여기에 더하여 해마가 다음과 같은 역할을 할 수 있음을 제안한다:

* **희귀하지만 중요한 사건(statistically infrequent but significant events)**을
* **‘표시(marking)’하거나, 강조하고**
* **기억 체계에서 우선권을 부여**하도록 만든다는 것

→ 이는 그러한 사건들이 **대다수의 일반적 경험에 의해 묻히는 것(swamped by typical experiences)**을 방지하고,
→ 오히려 **우선적으로 안정화되고(stabilized)**, **우선적으로 재생되어(replayed)**
→ 신피질에 통합될 수 있게 한다.

---

물론 이러한 재가중은 일반적으로는 **적응적(adaptive)**이지만,
특정 상황에서는 **부적응적(maladaptive)**일 수도 있다.

예:
**외상후 스트레스 장애(post-traumatic stress disorder, PTSD)**에서는
하나의 고유한 혐오 경험이
**지속적이고 우세한 표현(persistent and dominant representation)**으로 변질될 수 있으며,
→ 이는 **반복 재활성화(runaway reactivation)**에 의해 강화된다.

---

### 최근 실험적 발견들로부터 제기된 도전 과제들

(**Challenges Arising from Recent Empirical Findings**)

이 절에서는 **CLS 이론(complementary learning systems theory)**의 중심 명제(core tenets)에 대해 제기된 **두 가지 주요 도전(two significant challenges)**을 다룬다.
두 도전 모두 최근에 **계산 모델링(computational modeling)**을 통해 대응되었으며,
이론의 원칙들을 **확장(extend)**하고 **명확화(clarify)**하였다.

---

#### 1. 해마, 추론 및 일반화

(**The Hippocampus, Inference, and Generalization**)

첫 번째 도전은 다음 질문과 관련된다:

> 해마가 **특정 경험들(specific experiences)**로부터 출발하여
> 어떻게 **새로운 상황으로 일반화(generalize to novel situations)**할 수 있는가?

앞서 언급한 바와 같이, **CLS 이론**은 해마를 **빠른 학습 시스템(fast learning system)**으로 간주하며,
이는 **스파스한 활성 패턴(sparse activity patterns)**을 통해 **매우 유사한 경험들 간에도 중첩(overlap)**을 최소화한다.

이러한 대표 방식은 **구체적인 기억(memory of specifics)**을 지원하기에 적합하며,
**일반화(generalization)**는 **보완적 신피질 시스템(complementary neocortical system)**의 몫으로 간주되었다.

---

하지만 다음과 같은 실험적 증거들은 이 관점을 강하게 도전한다:

* 어떤 실험 과제에서는 피험자들이 **하나의 실험 세션 내 또는 직후에**,
* **연관된 경험들(related experiences)** 간의 연계(feature links)를 빠르게 활용하여
* **추론(inference)**을 수행하는 것이 관찰되었다 \[4,5,90–95].

→ 즉, 해마가 단순히 “개별 경험의 저장소” 그 이상일 수 있다는 것이다.

---

가장 대표적인 과제는 **쌍 연합 추론 과제(Paired Associative Inference, PAI)**이다 \[91,96–98].

이 과제에서는 다음과 같은 절차가 수행된다:

* 학습 단계: 피험자는 **객체 쌍(object pairs)** (예: AB, BC)를 본다.
  이 쌍들은 삼중 집합(triplets, 예: ABC)이나 여섯 개짜리 집합(sextets, 예: ABCDEF)에서 유도된다.

* 테스트 단계: 학습 중 함께 제시되지 않았던 항목들(예: A와 C, 또는 A와 F)에 대해
  **간접적 관계(indirect relationships)**를 **추론할 수 있는지** 평가한다.

해마가 이 과제에서 중요한 역할을 수행한다는 증거는,
해마가 **단일 에피소드 기반 처리(single-episode-based processing)**만을 수행한다는 기존 입장을 도전한다.

---

이러한 결과는 종종 다음과 같은 이론과 함께 해석되었다:

* **부호화 기반 중첩 모델(encoding-based overlap models)** \[4,95,99,100]
  → 이 관점은 해마가 AB, BC 같은 쌍들을 **결합(combine)**하거나 **통합(integrate)**하여
  **중첩된 표현(overlapping representations)**을 생성함으로써
  추론을 가능하게 한다고 본다.

---

하지만 CLS 기반의 **REMERGE 모델** \[5]은 다른 설명을 제시한다.

> 해마는 서로 별개의 기억 표현들(separate memory traces)을 유지하면서도,
> **재귀적 활성화(recurrent activation)** 메커니즘을 통해
> 새로운 연결을 추론할 수 있다.

즉, AB와 BC는 별도로 저장되지만,
시험 중 A와 C를 동시에 제시하면 이 둘이 **동시 활성화**되어
→ A–C 간 간접 관계를 유도할 수 있다.

이러한 기능은 해마 내에 존재하는 **재귀 회로(recurrent circuit)**를 통해 구현 가능하며,
이 회로는 시스템의 출력을 **다시 입력으로 순환(recircultate)**시킬 수 있다.
→ 관련 해부학적 및 생리학적 증거도 존재한다 \[101].

---

이처럼 **REMERGE**는 다음의 두 관점을 절충하고 있다:

* **관계 기억 이론(relational theory of memory)** \[29,102]
* **CLS 이론의 패턴 분리 가정(pattern-separated representations)** \[1,9,25–27,30,31,103,104]

→ 즉, 개별 에피소드는 분리되어 저장되지만,
→ **재생 중의 재귀 활성화**를 통해 **일반화와 추론**이 가능해진다는 것이다.

---

### Box 6. 해마 시스템 내 재귀를 통한 일반화

(**Generalization Through Recurrence in the Hippocampal System**)

**REMERGE 모델**(Figure I 참조) \[5]은
**상호작용 활성화 및 경쟁 모델(interactive activation and competition, IAC models)** \[163]과
**기억의 예제 기반 모델(exemplar models of memory)** \[108,164,165]을 결합한 구조이다.

이 모델은 해마 시스템의 복잡한 다단계 회로 구조를
두 개의 주요 층으로 단순화한 **추상화(abstraction)** 모델이다:

* **특징 층(feature layer)**: 내후각피질(**entorhinal cortex, ERC**)에 해당
* **결합 층(conjunctive layer)**: 해마 본체(**hippocampus proper**)에 해당

---

#### ● 결합 층의 국소 부호화 (Localist Coding in the Conjunctive Layer)

결합 층의 각 단위는 (예: "AB")
하나의 특정 경험(예: A와 B가 함께 제시된 경험)을 나타낸다.

→ 이는 실제 해마의 **DG/CA3 아구역에서의 스파스하고 분리된 표현(sparsely distributed pattern-separated codes)**을
**이상화(idealization)**한 것이다 (Boxes 2–4 참조).
→ 즉, REMERGE에서는 실제 뉴런 집단이 아닌 **하나의 단위(unit)**로 경험을 표현한다.

---

#### ● 핵심 원리: 대회로 재귀 (Big-loop Recurrence)

이 모델의 핵심 원리는 다음과 같다:

* **특징 층과 결합 층 사이에 양방향 흥분성 연결(bidirectional excitatory connections)**이 존재하며
* 이로 인해 시스템의 **출력(output)**이 **다음 입력(input)**으로 **재귀적으로 순환(recirculate)**될 수 있다.

→ 이 순환 구조는 **해마 본체와 ERC 간**, 그리고
→ **ERC와 신피질 간에 존재하는 재귀 회로(big-loop recurrence)**를 추상적으로 반영한다.

이 재귀는 다음과 같은 기능을 가능하게 한다:

* **초기 자극(initial probe)**이 들어오면
* 해당 항목을 포함하는 **과거의 경험들**이 결합 층에서 활성화되고
* 이로 인해 **새로운 특징 패턴**이 다시 특징 층에 생성되며
* 다시 결합 층으로 되돌아가 **관련된 다른 경험들**을 추가로 활성화하게 된다.
  → 이 과정을 반복하면 **관련 항목 간 간접 연결(indirect links)**이 자연스럽게 추론된다.

---

#### ● 예시: A–C 관계의 추론

예를 들어, A와 C가 시험 중 제시되었다고 하자.

* A는 AB 경험을, C는 BC 경험을 활성화
* AB와 BC는 공통 항목 B를 매개로 상호 간 강화
* B가 다시 AB와 BC를 활성화 → A, B, C가 모두 공존하는 안정된 상태(stable state) 도달
  → 결과적으로 **A와 C가 연결되어 있다는 일반화(generalized inference)**가 형성된다.

이 방식은 **더 긴 거리의 추론(longer-range inferences)**에도 확장 가능하다 (예: B–E 간 관계 등).
→ 자세한 사항은 \[5] 참조.

---

#### ● 모델의 수학적 관점

REMERGE는 수학적으로는 다음과 같은 방식으로 해석될 수 있다:

* **유사도 기반 연산(similarity computation)**을 **재귀적으로 반복**
* 기존의 예제 기반 모델들과 달리,
  → REMERGE는 **외부 입력(external input)**뿐 아니라
  → **이전 출력을 포함하는 새로운 입력**에도 유사도 연산을 수행함

→ 이로 인해 **단순한 유사성 기반 분류(classification)**를 넘어서
→ **고차 구조(high-order structure)**에 대한 **발견(discovery)**이 가능해진다.

---

#### 그림 설명 (Figure I)

모델 구조는 다음과 같다:

* 입력/출력 유닛: A–F
* 결합 유닛: AB, BC, CD, DE, EF 등 → 실제로 함께 제시된 항목쌍들
* 점선 화살표: 특징 유닛과 결합 유닛 간 양방향 연결
* 넓은 화살표: 결합 유닛들 간 상호 억제 (경쟁을 유도)

이 구조는 해마 내에서 이루어지는 **스파스한 결합 기억(sparse conjunctive memory)**과
**경험 간 상호 간섭 억제**를 단순화하여 표현한 것이다.

---

이러한 접근법은 **부호화 기반 중첩 모델(encoding-based overlap models)**과
**중요한 이론적 차이점(theoretical distinction)**을 갖는다.

* **중첩 모델들**은
  → **학습 중**에 항목 간의 **중복된 신경 표현(overlapping neural representations)**이 형성되어
  → **추론(inference)**이 가능해진다고 주장한다.

* 반면, **REMERGE 모델**은
  → 해마가 **초기 학습 시**에는 항목들을 **분리된(spaced apart)** 형태로 저장하지만
  → **시험 시(test time)**에 **재귀적 활성화(recurrent activation)**를 통해
  → **간접적 관계(inferred links)**를 유도한다.

이 두 이론은 **구체적인 실험 조건**에서 **서로 다른 예측을 내놓는다**. 예를 들어:

* **AB와 BC** 쌍을 학습할 때, **동시에 제시(simultaneous presentation)**하면
  → 중첩 모델은 A와 C가 이미 **공통된 표현으로 통합(integrated representation)**되어
  → 시험 시 더 쉬운 추론이 가능할 것이라 본다.

* 반면, **시간차 제시(sequential presentation)**나
  → **학습 시 A와 C의 간접 연결이 약하게 형성된 조건**이라면,
  → **REMERGE**는 **시험 시 활성화 동역학(dynamics of activation)**에 따라
  → 추론 성능이 달라질 것으로 예측한다.

---

또한, 최근의 실험적 발견들은
**해마의 뉴런들이 서로 중첩된 표현을 가질 수 있음**을 시사한다.
가장 대표적인 것은 **"개념 세포(concept cells)"** 또는
**"제니퍼 애니스턴 뉴런(Jennifer Aniston neurons)"**이다 \[92,105–107].

이러한 뉴런들은 다음과 같은 특성을 가진다:

* 동일 뉴런이 “제니퍼 애니스턴”, “리사 쿠드로”, “프렌즈(Friends)” 등
  **의미적으로 관련된 자극들**에 대해 반응함
* 즉, 하나의 뉴런이 **여러 개념에 중첩된 반응(overlapping response)**을 보이는 것이다

---

하지만 이 중첩성은 다음과 같이 해석될 수 있다:

1. **신피질로부터의 상향 입력(bottom-up input)**에 의해
   → 해마 뉴런이 여러 개념에 반응하는 것일 수 있음
   → 즉, **해마 내부의 표현은 여전히 분리되어 있을 수 있음**

2. 또는 **해마 CA1 또는 ERC와 같은 구역**에서는
   → **정말로 중첩 표현이 존재할 수 있음**

→ REMERGE 모델은 **스파스한 결합 표현(sparse conjunctive representations)**을
CA3에서 가정하고 있지만,
**CA1/CA3/ERC 간 차이**는 **더 정교한 계층적 모델(hierarchical models)**에서 표현 가능하다 \[5,31,103].

---

결론적으로, **REMERGE**는 기존 **CLS 이론의 패턴 분리 원칙**을 유지하면서도
**해마 내에서의 추론 능력**을 설명할 수 있는
**재귀 메커니즘 기반의 통합 이론(integrated recurrent mechanism)**을 제공한다.

---

다음은 두 번째 도전 과제인
**새로운 정보에 대한 신피질의 빠른 학습과 선택적 안정화(Rapid Neocortical Learning and Selective Stabilization)**로 이어집니다. 계속 번역해드릴까요?
계속해서 **두 번째 도전 과제: 신피질의 빠른 학습과 선택적 안정화(Rapid Neocortical Learning and Selective Stabilization)** 절을 전문용어 병기 방식으로 번역합니다.

---

### 두 번째 도전 과제: 신피질의 빠른 학습과 선택적 안정화

(**Rapid Neocortical Learning and Selective Stabilization**)

**CLS 이론(complementary learning systems theory)**에서 제시한 중심 가정 중 하나는 다음과 같다:

> **신피질(neocortex)**은 **느린 속도(slow rate)**로 학습해야
> 기존 지식 구조(existing knowledge structures)를 **망가뜨리지 않고**
> **새로운 정보를 통합**할 수 있다.

이러한 관점은 다음을 통해 **경험적으로 지지**받는다:

* 신피질 뉴런의 **장기 강화(long-term potentiation, LTP)** 유도에 필요한
  **강한 반복 자극(repeated high-frequency stimulation)** \[109,110]

---

하지만 이 가정은 다음과 같은 **새로운 실험 결과**에 의해 **도전**을 받는다:

* 인간은 어떤 정보를 **단 1\~2회의 노출만으로도 학습**할 수 있다 \[111–114]
* 특히, 정보가 다음 중 하나일 경우 더욱 그러하다:

  * **중요하거나(significant)**
  * **흥미롭거나(emotionally salient)**
  * **주의(attention)**를 끌거나
  * **신규성(novelty)**을 띠는 경우

이러한 발견은 신피질이 **경우에 따라 빠르게 학습할 수 있음**을 시사하며,
CLS 이론이 주장하는 “항상 느린 학습”이라는 조건과 충돌할 수 있다.

---

우리는 이 문제를 해결하기 위한 **확장된 CLS 모델**을 제안한다:

> **신피질 학습의 속도(rate of learning)**는
> **단일한 값이 아니라**, **상황에 따라 조절되는 변수(context-sensitive variable)**이다.

즉, 특정 조건에서는 신피질이

* 빠르게 학습할 수 있으며,
* 동시에 **기존 지식 구조를 유지하면서도 안정적인 통합(stable integration)**을 달성할 수 있다.

---

이러한 유연한 학습 조절은 다음 요소에 의해 가능할 수 있다:

1. **주의(attention)**
2. **동기(motivation)**
3. **보상 시스템(reward systems)**
4. **신경조절계(neuromodulatory systems)**

   * 예: 아세틸콜린(acetylcholine), 도파민(dopamine), 노르에피네프린(norepinephrine) 등

→ 이러한 신호들은 신피질 내 학습 속도 또는 가소성(plasticity)의 정도를
**선택적으로 증가**시키는 역할을 할 수 있다 \[83,84,86,115].

---

또한, **최근 계산 모델들**은 다음을 보여준다:

* **지식 구조(knowledge structures)**가 이미 충분히 **일반화되어 있거나 추상화되어 있다면**,
  → 새로운 경험을 추가하는 것은 기존 구조를 **망치지 않고** 오히려 **보완할 수 있다** \[116].

예:
새로운 개가 "짖는다(barks)"는 사실을 학습할 때,
이미 개와 관련된 구조적 지식(예: 네 발, 꼬리, 포유류 등)을 갖고 있다면
→ "짖음"이라는 속성을 쉽게 통합 가능

---

우리는 이러한 현상을 **선택적 안정화(selective stabilization)**라고 부른다:

> **새로운 지식 중 일부**는
> 기존 구조에 더 잘 맞기 때문에
> **더 빠르게, 더 쉽게 통합**되며
> 이는 **지식의 자기조직화(self-organizing knowledge acquisition)**를 가능하게 한다.

이 개념은 **CLS 이론**의 핵심 개념이었던
**느리고 반복적인 신피질 학습**의 필요성에 대한
**보다 정교한 조정(refinement)**으로 이해할 수 있다.

---

### 결론

(**Conclusion**)

이 글에서는 **상호보완 학습 시스템 이론(Complementary Learning Systems theory, CLS)**의
과거, 현재, 미래를 개관하였다.

초기 CLS 이론은 다음과 같은 중심 가정을 담고 있었다:

> **기억(memory)**과 **학습(learning)**은
> 서로 다른 속도와 대표 방식(representation formats)을 가진
> **두 개의 상호보완적 시스템(two complementary systems)**에 의해 수행된다.
> 이 시스템들은
>
> * **해마(hippocampus)**와
> * **신피질(neocortex)**이라는 두 주요 구조에 의해
>   생물학적으로 실현된다.

---

이 이론은:

* **기억 통합(memory consolidation)**
* **신경 손상 시의 기억 손실 현상(amnesia after brain damage)**
* **신피질의 점진적인 개념 학습(gradual acquisition of cortical knowledge)** 등
  다양한 현상을 성공적으로 설명해왔다.

---

하지만 이후 수십 년간의 연구는 다음과 같은 **새로운 질문과 확장 요구**를 제기하였다:

1. **해마는 단기 기억의 저장소인가, 아니면 그 이상인가?**
   → 해마는 **추론(inference)**, **일반화(generalization)**, **계획(planning)**까지 수행한다.

2. **신피질은 느린 학습만 가능한가?**
   → 특정 조건에서는 **빠른 학습(fast learning)**과 **선택적 안정화(selective stabilization)**도 가능하다.

3. **재생(replay)은 단순한 복원인가, 아니면 창조적 재조합인가?**
   → 재생은 **보상 편향(reward bias)**, **지름길 생성(shortcut generation)**, **가상 시뮬레이션(simulation)** 기능을 수행할 수 있다.

---

이에 따라, 우리는 CLS 이론을 다음과 같이 확장하여 제안한다:

* 해마는 단순한 **기억 저장 장치**가 아니라,
  → **의미 기반 선택(significance-guided selection)**과
  → **표현의 재가중(reweighting of experiences)**을 수행하는 **인지적 허브(cognitive hub)**이다.

* 신피질은 느린 학습만을 담당하는 것이 아니라,
  → 상황에 따라 **학습 속도와 안정화 강도**를 **조절할 수 있는 유연한 시스템**이다.

---

이러한 확장된 CLS 프레임워크는 다음을 설명할 수 있는 강력한 틀을 제공한다:

* **기억과 일반화의 상호작용(interaction between memory and generalization)**
* **단발 경험(one-shot experience)**의 영향력
* **의미 기반 학습(significance-based learning)**
* **창발적 개념 형성(emergent concept formation)**
* **계획과 사고의 기반으로서의 기억(memory as the basis of thought and planning)**

---

향후 연구에서는 다음과 같은 방향이 중요하다:

1. **해마와 신피질 간 상호작용의 메커니즘 구명**
2. **재생의 시점별 기능 분석(time-specific functions of replay)**
3. **인지 기능에서의 해마의 역할 확대(e.g., imagination, simulation, creativity)**
4. **신경조절(neuromodulation)**이 학습과 통합에 미치는 영향
5. **인간과 인공지능 시스템 간의 통합 학습 모델 개발**

---

CLS 이론은 단순한 기억 이론이 아니라,
**지능(intelligence)**과 **학습(learning)**의 본질을 이해하기 위한
**뇌 기반 모델(brain-based model)**로서
→ 앞으로도 계속 확장되고 발전할 것이다.

---

