**"Bridging Generative Networks with the Common Model of Cognition"**
---

### 초록 (Abstract)

본 논문은 인공지능(AI) 분야에서 **대규모 생성 네트워크 모델(generative network models)**에 **공통 인지 모델(Common Model of Cognition, CMC)**을 적용하기 위한 이론적 틀을 제시한다. 이를 위해, 공통 모델 내의 모듈들을 **그림자 생산 시스템(shadow production systems)**으로 재구조화하고, 이들을 중심이 되는 **생산 시스템(central production system)**의 주변(peripheral)에 배치하여, 그림자 생산 시스템의 출력에 기반해 고차원 추론(higher-level reasoning)을 수행하도록 한다. 이러한 새로운 구조를 공통 인지 모델 내에 구현함으로써, **인지 아키텍처(cognitive architectures)**와 **생성 신경망(generative neural networks)** 사이의 원활한 연결이 가능해진다.

---

### 서론 (Introduction)

지능형 시스템(intelligent systems)은 **전통적 인공지능(Good Old-Fashioned Artificial Intelligence, GOFAI 또는 "기호 기반(symbolic)")** 추론과 **연결주의 통계학습(connectionist statistical learning)**(예: Hitzler 외, 2022)을 모두 갖춤으로써 상당한 견고성(robustness)을 획득한다. 그러나 이 둘을 어떻게 통합할지에 대한 합의는 존재하지 않는다. 덜 탐색된 방법 중 하나는, **생성 AI 모델(generative AI models)**과 **인지 아키텍처(cognitive architectures)**를 하나의 **하이브리드 시스템(hybrid system)**으로 통합하는 것이다. 인간 인지의 구조를 모델링하기 위한 유력한 후보는, 이전에는 **표준 마음 모델(Standard Model of the Mind)**로 불렸던 **공통 인지 모델(Common Model of Cognition, CMC)**이다(Laird, Lebiere, and Rosenbloom 2017). 그러나 현재 CMC는 낮은 수준의 연결주의 요소들을 인지 수준에서 해석 가능하게 만들 수 있는 방법이 결여되어 있다.

공통 인지 모델(CMC)은 인간 인지가 계산적으로 어떻게 작동하는지를 설명하며, **대규모 신경과학 데이터(neuroscience data)**를 통해 그 타당성이 입증되어왔다(Stocco 외, 2021). 반면, 대부분의 **생성 신경망(generative neural networks)**은 생물학적 대응성(biological correspondence)에 의해 제약받지 않고, 대신 지능적인 출력을 생성하는 실용적 접근(pragmatic approach)을 취한다.

**인지 모델링(cognitive modelling)**과 **인공지능(artificial intelligence)**은 목표가 서로 다르다. 전자는 인간 및 동물의 행동을 설명하고 예측하는 데 중점을 두는 반면, 후자는 인간의 개입 없이 문제를 해결하고 과제를 수행하는 데 초점을 맞춘다. 그럼에도 불구하고, 인지 모델은 최신 **딥러닝 접근법(deep learning approaches)**과의 통합으로부터 이점을 얻을 수 있다. 왜냐하면 생성 네트워크가 해결하는 많은 과제는, 인지 모델링에서 세부적인 처리 모델이 결여된 과제들—예: **지각(perception)**, **상상(imagination)**, **자연어 처리(natural language processing)**—이기 때문이다. 이러한 이유로, 대규모 생성 네트워크는 인간이 이러한 과제를 수행하는 방식을 설명할 수 있는 **후보 인지 모델(candidate cognitive models)**로 이해될 수 있다.

그러나 **대규모 언어 모델(large neural language models)**과 같은 생성 네트워크는 **형식 논리(formal reasoning)** 능력에 있어서 중대한 한계를 보인다는 것이 입증되었다(Helwe, Clavel, and Suchanek 2021). 이는 **구조화된 추론(structured reasoning)** 및 **문제 해결 과정(problem solving processes)**을 따르도록 설계된, 전통적인 “언어와 논리(language and logic)” 기반 접근과 대조된다(Shaw 외, 1958; West and Nagy 2007). 따라서 전통적인 인지 모델링 접근법과 생성 네트워크의 통합은 인간 행동의 전체 스펙트럼을 모델링할 수 있는 아키텍처를 만들어낼 수 있으며, 단일 AI 시스템이 해결 가능한 문제의 범위 또한 넓힐 수 있다.

우리는 **딥러닝(deep learning)**을 전통적 인지 모델링과 연결하기 위해, 공통 인지 모델(CMC)에 대한 상당한 구조적 조정을 제안한다. 이를 통해 CMC 모델이 보다 진보된, 대규모 인지 능력(cognitive abilities)을 갖추도록 한다. 본 논문에서는 먼저 CMC와 **ACT-R 인지 아키텍처(ACT-R cognitive architecture)**(Anderson and Lebiere 1998)에 대해 간략히 논의하고, 이후 이를 어떻게 재구성할 수 있는지 설명한다.

본 논문의 핵심 기여는, **ACT-R이 모듈(module)**을 개념화하는 방식을 새롭게 정식화(reformulate)한 것이다. ACT-R은 인간 인지를, 지각(perception), 운동(motor), 언어(language) 등 특정한 인지 능력을 담당하는 모듈들과, **절차 기억(procedural memory)** 및 **작업 기억(working memory)**으로 구성된 중심 실행 시스템(central executive)이 함께 작동하는 것으로 본다. 그러나 이러한 모듈들이 해당 인지 기능을 어떻게 구현해야 하는지에 대한 표준은 존재하지 않으며, 실제로는 임의적 방식(ad hoc manner)으로 구현되고 있다.

이에 우리는, ACT-R 및 기타 CMC 아키텍처에서 모듈을 구현하는 표준화된 접근법을 제안한다. 이 접근법에서 각 모듈은 **사전 학습된 생성 네트워크(pre-trained generative networks)**, 네트워크를 관리하는 **생산 시스템(production system)**, 그리고 네트워크와 생산 시스템 사이를 연결하는 **기억 시스템(memory system)**으로 구성된다.

---

### 공통 모델의 구성 요소 (Components of the Common Model)

**공통 인지 모델(Common Model of Cognition, CMC)**은 인간 수준의 지능(human-like intelligence)에 필수적인 구성 요소들에 대해 **여러 인지 아키텍처(cognitive architectures)** 간의 수렴(convergence)을 보여준다. 공통 모델은 다섯 가지 모듈을 포함한다: **지각(perception)**, **작업 기억(working memory)**, **운동(motor)**, **명시적 기억(declarative memory)**, 그리고 **절차 기억(procedural memory)**이다. 이 중 절차 기억은 공통 모델이 작동하는 방식에서 중심적인 역할을 하며, 이는 작업 기억의 내용에 기반하여 다른 모듈들에게 반응하고 지시를 내린다.

절차 기억을 구성하는 직관적인 방식은 **생산 시스템(production system)**을 사용하는 것이다. 생산 시스템은 공통 모델에서 설명하는 기본 기능들을 구현하는 오래된 방법이며, 따라서 본 논문에서는 보다 복잡한 시스템이 사용될 수 있다는 단서를 두고 이 용어를 사용한다. 이 방법은 **ACT-R**에서 채택되었지만, **SOAR**(Laird 2012), **Sigma**(Rosenbloom, Demski, and Ustun 2016)와 같은 다른 공통 모델 아키텍처들과는 차이를 보인다. 본 논문에서는 공통 모델에 대한 논의를 **ACT-R 이론**을 중심으로 진행한다.

---

### 청크 (Chunks)

**청크(chunk)**는 공통 모델에서 모듈 간의 의사소통 단위로 작동하며, 일반적으로 **명제적 정보(propositional information)**를 전달한다(Laird, Lebiere, and Rosenbloom 2017). 예를 들어 `name:Fido isa:dog breed:labrador`와 같은 청크는 이런 구조를 보여준다. 청크는 또한 장기 기억(declarative memory)으로부터 정보를 요청하는 데에도 사용된다(Stewart 2007). 예컨대 `name:? isa:dog breed:labrador`라는 청크는 첫 번째 슬롯의 누락된 값을 요청하며, 다른 슬롯들의 값을 기준으로 일치하는 어떤 청크든 검색할 수 있다.

청크는 어떤 모듈에서도 생성될 수 있으며, 모듈 간에는 **버퍼(buffer)**에 청크를 배치함으로써 전달된다. 청크의 구조는 중요하다. 왜냐하면 청크의 구조와 내용이 절차 기억 내에서의 **생산 규칙(production rule)**의 매칭 조건을 유발하기 때문이다. 청크는 기호 구조(symbolic structures), **홀로그램 벡터(holographic vectors)**(청크 구조를 해석해낼 수 있음, Kelly et al. 2020; Kelly, Kwok, and West 2015 참조), 혹은 **신경 신호(neural signals)**로 부호화될 수 있으며(이 또한 홀로그램 벡터와 유사하게 작동함, Eliasmith 2013 참조), 다양한 표현 방식이 가능하다.

---

### 버퍼 (Buffers)

**ACT-R**(Anderson and Lebiere 1998)에서는, **버퍼(buffer)**가 중심 생산 시스템과 주변 모듈 간의 정보를 전달하는 역할을 한다. 모든 버퍼는 함께 아키텍처의 **작업 기억(working memory)**을 형성한다. 버퍼링(buffering)은 데이터를 임시로 특정 메모리 공간에 저장함으로써, 다양한 구성 요소나 시스템 간에 데이터 처리, 전송 또는 정보 교환을 가능하게 하는 것이다.

작업 기억에는 서로 다른 모듈로부터, **병렬적(parallel)**이고 **다양한 속도**로 정보가 입력된다. 중심 생산 시스템이 **50ms 주기(cycle)**로 작동하기 위해서는, 입력된 정보가 미리 버퍼링되어 있어야 한다.

---

### 모듈과 명시적 기억 (Modules and Declarative Memory)

공통 모델(Laird, Lebiere, and Rosenbloom 2017) 내에서, **주변 모듈(peripheral modules)**은 **인지적 및 신경 기능(cognitive and neural functions)**을 구분하는 것으로 나타난다(도표 Figure 1 참조). 이러한 모듈에는 **명시적 기억 모듈(declarative memory module)**, **지각 모듈(perception module)**, **운동 모듈(motor module)**이 포함되며, 최근에는 **감정 모듈(emotion module)**도 제안되고 있다.

모듈은 일반적으로 **불완전한 정보가 포함된 청크 템플릿(chunk template)**의 형태로, 절차 기억으로부터 요청을 받는다. 이러한 요청은 시각 검색(visual search), 운동 행동(motor actions), 감정 평가(emotional evaluations) 등을 유발할 수 있다. 주변 모듈의 응답은 다시 청크로 변환되어 각 모듈에 연관된 버퍼에 배치되며, 이는 절차 기억이 정보를 접근할 수 있도록 해준다.

> **\[Figure 1]** 공통 모델 아키텍처 (The Common Model Architecture)

명시적 기억 모듈은 이전에 저장된 청크들의 **저장소(warehouse)**로 기능하며, 요청이 있을 경우 이를 검색한다. 중심 생산 시스템은 다양한 주제에 대한 정보를 요청할 수 있으며, 명시적 기억은 적절한 청크를 검색해 버퍼에 배치한다. 이 상호작용(interplay)의 결과로, 인지는 **미리 정의된 규칙(predefined rules)**에 따라 행동을 유도하는 **생산(productions)**에 의해 작동하기도 하고, **저장된 정보(stored information)**를 참조하는 명시적 기억에 의해 작동하기도 한다. 이 조합은 공통 모델 내에서 **유연하고 역동적인 인지 처리(flexible and dynamic cognitive processes)**를 가능하게 만든다.

---

### 생산 규칙 (Production Rules)

**생산 규칙(production rule)**의 기본 구조는 **조건-행동 쌍(conditional-action pairing)**이다(Stocco et al. 2021). 규칙은 특정 조건이 충족되었을 때 수행할 동작을 명시한다. 이는 흔히 “if-then” 규칙이라고도 불리며, 여기서 “if” 부분은 **버퍼(buffer)**의 내용과 일치하는 조건이고, “then” 부분은 지정된 동작을 수행한다.

버퍼는 시스템의 작업 기억(working memory)으로, 다양한 생산(productions)의 **입출력(input/output)** 역할을 수행한다. 만약 조건이 버퍼의 내용과 일치하면, 그 규칙은 정해진 동작을 실행한다. 이 때의 동작은 주변 모듈(peripheral modules)과의 통신이나 버퍼의 내용을 수정하는 명령일 수 있다.

여러 생산 규칙이 동시에 일치(match)할 경우, **가장 높은 효용값(utility value)**을 가진 규칙이 선택된다. 이 전체 과정은 인지의 단일 주기(single cycle of cognition)를 구성한다. 일반적으로 생산 규칙은 사전에 정의된 규칙을 지칭하지만, 이 규칙들은 매칭 시점에 생성되거나 시간이 지나며 학습되어 발전할 수도 있다. 공통 모델 아키텍처들은 고정된 생산 규칙을 넘어서기 위한 다양한 접근을 채택한다(Kieras and Meyer 1997; Laird 2012; Laird, Lebiere, and Rosenbloom 2017).

에이전트(agent)의 현재 상황은 버퍼들에 부호화되어 있으며, 생산 규칙은 대안 선택들 간의 선택 과정을 나타낸다(Newell 1973). 특정 상황에서는, 예컨대 반응 속도가 중요한 비디오 게임처럼, 하나의 생산 규칙만으로 선택이 이루어지는 경우도 있다. 이 경우 특정 신호가 **미리 학습된 반응(well-learned responses)**을 유발한다(Greve, Reid, and West 2020).

그러나 보다 일반적으로는, **여러 생산 규칙이 순차적으로 작동**하여 하나의 선택 과정에 필요한 여러 단계를 수행하게 된다. 예를 들어, 생산 규칙은 특정 **의사결정 전략(decision-making strategy)**을 선택하거나, **추가 정보를 요청(memory retrieval)**하는 데 활용된다. 이러한 생산 규칙의 연쇄적 작동은 알고리즘 수행, 논리적 사고(logical thinking), 인과 추론(causal reasoning), 휴리스틱(heuristics) 등을 구현할 수 있다.

---

공통 인지 모델(CMC)에서의 생산 규칙의 주요 특성은 작동 방식의 세부사항보다는 **공통적으로 공유되는 세 가지 속성**에 있다.

1. **순차적 작동(sequential operation)**: 생산은 순차적으로 작동하며, 동시에 하나의 생산만이 실행된다. 이는 **직렬 병목(serial bottleneck)**이라 불리는 현상을 유발한다. 일부 아키텍처(예: Epic architecture, Kieras and Meyer 1997)는 병렬 생산(parallel productions)을 주장하지만, 실제로는 여러 생산이 하나의 큰 생산으로 결합되어 여전히 직렬 병목을 유지한다.

2. **타이밍(timing)**: 생산의 시간 척도는 **50ms**로 설정되어 있다. 이는 Newell(1994)이 제시한 **인지 대역(cognitive band)**의 **의도적 행위(deliberate act)**에 해당하며, 그의 시스템 수준 체계(system levels framework)의 시간 척도에 부합한다(Table 1 참조). Newell은 일반적인 신경 타이밍 원칙에서 로그 척도(logarithmic scaling)를 통해 약 100ms의 시간 척도를 제안했고, CMC 모델은 **인간 반응 시간(human reaction times)**과 **기저핵(basal ganglia)** 모델과의 일치성을 바탕으로 50ms를 채택하였다(Senft et al. 2016; Stewart, Choo, and Eliasmith 2010; Stocco et al. 2021).

3. **기호 처리(symbolic processing)와의 대응성**: 일반적으로 생산은 **지식의 단위(units of knowledge)**로서의 청크(chunk)를 조작한다. 이 청크는 이산 기호(discrete symbols), 연속값 벡터(continuous-valued vectors), 또는 신경 활동(neural activity)으로 표현될 수 있다(Kelly et al. 2020; Rutledge-Taylor et al. 2014; Stewart, Choo, and Eliasmith 2010). 그러나 생산은 항상 **이진 선택(binary choice)**을 강제한다: 생산은 현재 상황과 **일치(match)**하거나 **일치하지 않음(non-match)** 중 하나로만 반응한다. 따라서 **모호한 자극(ambiguous stimuli)**은 **모호하지 않은 반응(unambiguous responses)**을 만들어낸다.

예컨대, 에이전트가 어떤 동물이 **큰 개(large dog)**인지 **작은 곰(small bear)**인지 불확실할 때, 에이전트는 **접근하거나(approach)** 혹은 **멀리 떨어지거나(stay away)** 하는 둘 중 하나를 선택하지, 이 둘을 혼합한 반응을 하지 않는다.

---

### 그림자 생산 (Shadow Productions)

**그림자 생산 시스템(Shadow production system)**은 중심 생산 시스템(central production system)과 마찬가지로, **“if-then” 규칙(if-then rules)**의 집합으로 구성되며, 기억(memory)의 내용에 반응하여 규칙이 활성화되고, 그에 따라 기억의 내용을 수정한다. 그러나 그림자 생산은 중심 실행 체계(central executive)에 위치하는 것이 아니라, **지각(perception)**, **운동(motor)**, **감정(emotion)** 등과 같은 **주변 인지 모듈(peripheral cognitive modules)** 내에 위치한다.

비록 그림자 생산이 CMC의 공식 구성 요소는 아니지만, 이전의 CMC 모델들에서 효과적으로 사용되어 왔다(West and Young 2017). 이 개념은 특히 **편도체(amygdala)**로부터의 감정(emotion)이 어떻게 인지 수준에서 행동을 방해하거나 영향을 주는지를 설명하기 위해 개발되었다. 그림자 생산은 **중심 생산 시스템의 보조 시스템(auxiliary system)**이며, 중심 생산과 **병렬적으로(parallel)** 작동하지만, **직렬 병목(serial bottleneck)**을 방해하지는 않는다.

그림자 생산의 주요 역할은, 예컨대 **위협 탐지(threat detection)**와 같은 하위 수준의 신호를 모니터링하는 것이다. 그림자 생산은 작업 기억의 버퍼로부터 정보를 받아, 위협 평가(threat evaluation)의 문맥(context)을 제공할 수 있다. 그림자 생산이 위협의 존재를 감지했다고 판단하면, 중심 생산 시스템이 접근할 수 있는 버퍼에 해당 정보를 배치한다.

그림자 생산은 이론적으로 **모든 버퍼를 참조하여(match)** 작동할 수 있지만, **하나의 버퍼에만 기록(write)**할 수 있다. 반면 중심 생산 시스템의 생산 규칙은 **여러 버퍼에 기록**할 수 있다. 따라서 중심 생산 시스템은 **전체 과제(overall task)**를 관리하고, 그림자 생산은 **주변 모듈(peripheral modules)**로 표현되는 과제의 다양한 측면을 관리한다(Figure 1 참조). 종합하면, 그림자 생산은 주변 모듈로부터 오는 **상향(bottom-up)** 정보를 관리하며, 중심 생산 시스템은 과제, 특히 **방해(interruptions)**를 포함한 상위(top-down) 제어를 담당한다.

---

### 뉴웰의 수준 체계 (Newell’s Levels)

뉴웰(Newell, 1994)은 그의 **시스템 수준 체계(system levels scheme)**에서, 뇌(brain)를 이해하기 위한 **가장 낮은 수준의 밴드(lowest system levels band)**는 **뉴런(neuron)**과 관련된 언어와 수학(예: 네트워크, 활성화, 벡터 등)으로 설명되는 것이 가장 적절하다고 보았다. 뉴웰은 이것이 **인지 대역(cognitive band)** 내의 시스템 수준들과는 다르다고 보았으며, 후자는 **계산(computation)**과 **선택(choice)**의 언어—예: 청크(chunk), 기호(symbols), 알고리즘(algorithms), 휴리스틱(heuristics)—로 설명된다고 하였다.

기능적으로 보면, **생성 신경망(generative neural networks)**의 기능은 **예측(prediction)**이라 말할 수 있다. 그러나 일부 이론가들은 모든 인간 인지가 예측 과정(predictive process)이라고 주장한다(즉, 무엇이 다음에 올지를 예측하고, 특정 상황에서 어떤 정보가 유용할지를 예상함; Clark, 2013; Hutchinson and Barrett, 2019; Parr, Pezzulo, and Friston, 2022). 본 논문은 전자의 주장에는 동의하지만, 후자의 주장에는 동의하지 않는다. 즉, **신경망은 예측을 잘 수행하지만, 인지는 단순한 예측 이상의 것이다.**

즉, **인지(cognition)**는 **기호 기반 추론(symbolic reasoning)**을 통한 **의사결정(decision)**을 요구한다. 뉴웰(1994)이 설명한 인지 수준(cognitive level)의 설명 방식은 전통적으로 **기호 기반 선택(symbolic choice)**을 특징으로 하며, 이를 **생산(productions)** 형태로 나타낸다. 종합하면, 인지 수준 접근법은 **기호 기반 의사결정(symbolic decision-making)** 모델링에 적합하고, **신경 수준(neural level)** 접근법은 **비기호 기반 예측(non-symbolic prediction)** 모델링에 적합하다. 따라서 **예측 처리(predictive processing)**의 계산적 이점과 **기호 기반 의사결정(symbolic decision-making)**의 인지 수준 처리를 모두 활용하는 **통합 프레임워크(unified framework)**가 필요하다.

실용적으로, 본 논문은 프레임워크의 각 부분을 **기호(symbolic)** 혹은 **연결주의(connectionist)**로 **하이브리드(hybrid)** 방식으로 설명하고 코딩할 것을 제안한다. **기호와 벡터 간 변환(tokenization and detokenization)**은 **홀로그램 명시적 기억(Holographic Declarative Memory, HDM)** 시스템과 유사한 방식으로 처리할 수 있다(Kelly et al. 2020; Kelly, Kwok, and West 2015; Kelly and Reitter 2017). 이 시스템에서는 **청크된 명제 정보(chunked propositional information)**를 담은 벡터를 기호 청크로 **압축 해제(unpack)**할 수 있고, 기호 청크를 다시 벡터로 **압축(pack)**할 수 있다.

또한, 이 전체 시스템은 **신경적 형태(neural form)**로도 구현될 수 있다(예: **NENGO**를 활용). 이 경우 **압축 해제(unpacking)**는 **합성 벡터(composite vector)**로부터 **특정 벡터**를 추출하는 것을 의미한다.

---

> ⬇️ 표: 인간 행동의 시간 척도에 대한 뉴웰(1994)의 시스템 수준 및 밴드

| **시간 척도(Time)** | **단위(Unit)** | **레벨(Level)**          | **밴드(Band)**    |
| --------------- | ------------ | ---------------------- | --------------- |
| 10⁷             | 개월(months)   |                        | 사회적(Social)     |
| 10⁶             | 주(weeks)     |                        |                 |
| 10⁵             | 일(days)      |                        | 과제(Task)        |
| 10⁴             | 시간(hours)    |                        |                 |
| 10³             | 10분          |                        | 합리적(Rational)   |
| 10²             | 분(minutes)   |                        |                 |
| 10¹             | 10초          | 단위 과제(unit task)       |                 |
| 10⁰             | 1초           | 작업(operations)         | 인지(Cognitive)   |
| 10⁻¹            | 100ms        | 의도적 행위(deliberate act) |                 |
| 10⁻²            | 10ms         | 신경회로(neural circuit)   | 생물학(Biological) |
| 10⁻³            | 1ms          | 뉴런(neuron)             |                 |
| 10⁻⁴            | 100μs        | 세포소기관(organelle)       |                 |

---

### ChatGPT의 예시와 중간 처리 계층(Middle Space)에 대한 비유

본 논문에서 제안하는 시스템의 작동 방식을 설명하기 위해 **ChatGPT(OpenAI, 2022)**의 사용을 예시로 들어보자.

사람이 ChatGPT를 사용할 때, **프롬프트(prompt)**를 입력하고, 그에 대응하는 **자연어 출력(natural language output)**을 기다린다. ChatGPT는 우선 프롬프트에서 **가장 중요한 단어들**을 선택하고, 이를 **토큰화(tokenization)**하여 모델 입력에서 해당 토큰의 가중치를 높인다. 이후, 다음 토큰 단어를 **예측(prediction)**하고, 선택된 단어를 프롬프트에 추가한 뒤, 이 과정을 반복한다.
결과적으로, 선택된 **토큰화된 응답(tokenized response)**은 다시 **자연어(natural language)**로 **디토큰화(detokenization)**된다. 이 과정을 반복하여 응답이 완성된다.

이후 인간은 생성된 결과의 **의미를 평가(evaluate the meaning)**하고, 이를 수용하거나 수정 요청을 하거나, 더 나은 프롬프트를 만드는 방식으로 반응한다. 이 예시에서, **인간은 기호 기반 추론자(symbolic reasoner)**이며, ChatGPT는 **예측 시스템(prediction system)**이다.

그러나 여기서 중요한 것이 하나 빠져 있다.
ChatGPT 내부에는 **토큰화(tokenization)**, **어텐션(attention)**, **업데이트(update)**, **반복(iteration)** 등과 같은 **구체적인 동작들(specific actions)**이 존재하는데, 이들은 **예측(predictive)**이 아니라, **네트워크로부터 정확한 응답을 끌어내기 위해 설계된 저수준 명령(low-level instructions or rules)**이다.
본 논문에서 제안하는 방식은, 바로 이러한 **중간 계층(middle space)**을 **공통 인지 모델(Common Model of Cognition)**에 추가하는 것이다.

---

### 제안된 프레임워크 (Proposed Framework)

**공통 인지 모델(CMC)**은 **각 모듈(module)**이 그에 해당하는 **생성 네트워크(generative network)**와 연결되도록 하여, 생성 네트워크와 CMC를 **직접적으로 연결**할 수 있다(그림 Figure 2 참조).

이런 방식은, 예를 들어 **SAL 인지 아키텍처(SAL cognitive architecture)**처럼, **ACT-R** 내부에 **신경망(neural network)**을 모듈로 삽입하는 방식을 통해 구현될 수 있다(Lebiere et al. 2008).

그러나 Figure 2의 **파이프라인 아키텍처(Pipeline Architecture)**처럼 단순 연결만 할 경우, **중심 생산 시스템(main production system)**이 만든 **직렬 병목(serial bottleneck)**에 **과도한 부하(heavy load)**가 걸릴 수 있다.

이에 본 논문은, 공통 인지 모델을 **보다 근본적으로 재구성(re-conceptualize)**하는 **대안적 접근(alternative proposal)**을 제시한다(그림 Figure 3 참조).

---

#### 1. 중간 기억(Middle Memory, MM)

우리는 CMC와 여러 생성 네트워크 사이에 **인터페이스 역할**을 수행하는 **중간 기억(Middle Memory, MM)**을 제안한다. MM은 **네트워크들로부터 입력받은 벡터(vectors)**를 수신하며, 이 벡터는 해당 네트워크가 “유용할 것이다”라고 예측한 정보(예: 다음 단어 등)를 나타낸다.

MM은 **다양한 양상(modality)**의 벡터들(예: 시각, 언어, 감정 등)을 모두 수신하며, 이는 다음 두 시스템과 유사한 역할을 한다:

* **ACT-R**의 **명시적 기억(Declarative Memory, DM)**
* **Soar**의 **작업 기억(Working Memory, WM)**

MM은 각 벡터에 **활성화값(activation values)**을 부여하여, 활성화값이 높은 벡터일수록 **작업 기억(working memory)**에 전달되어 중심 생산 시스템에서 사용될 확률이 높아지도록 한다. 이 **활성화값**은 다음 요인에 따라 결정된다:

* **최근성(recency)**
* **빈도(frequency)**
* **작업 기억에서의 확산 활성화(spreading activation)**

이는 인간과 유사한 제약을 도입하기 위한 조치이다.

또한, Soar WM과 ACT-R DM에서처럼, 절차 기억(procedural memory)은 MM 내에 **명제 청크(propositional chunks)** 형태로 **그래프 구조(graph structures)**를 저장할 수 있다.
우리는 **예측 벡터(prediction vectors)**와 **그래프 기반 의미(graph-based understanding)**를 MM 내에 혼합하여 저장함으로써 **시너지 효과**를 얻을 수 있다고 보며, 물론 이 둘을 분리하여 저장할 수도 있다.

---

#### 2. 모든 CMC 모듈을 그림자 생산 시스템으로 모델링

우리는 **절차 기억(procedural memory)**과 **작업 기억(working memory)**을 제외한 **공통 인지 모델(CMC)**의 모든 모듈을 **그림자 생산 시스템(shadow production systems)**으로 모델링할 것을 제안한다.
이러한 그림자 생산은 **작업 기억(Working Memory, WM)**과 **중간 기억(Middle Memory, MM)**의 정보를 참조(match)함으로써 활성화된다. 이때:

* **작업 기억(WM)**은 시스템의 현재 초점(current focus)에 대한 문맥(context)을 제공하고,
* **중간 기억(MM)**은 **네트워크가 예측한 정보(predictions of what will be useful)**와 **상황에 대한 그래프 기반 이해(graph-based understanding)**를 혼합하여 제공한다.

이 모델에서는 **표현 방식(representation)** 자체에는 초점을 두지 않는다. MM 내의 모든 정보는 다음 세 가지 방식 중 **어느 하나로 통일하거나**, **혼합**할 수 있다:

* 모두 **벡터(vector)**로 변환
* 모두 **기호적 명제(symbolic propositions)**로 변환
* **기호와 벡터를 혼합한 형태**

생산 규칙의 매칭 조건은 다양한 형식을 혼합할 수 있기 때문에, 표현 방식의 선택이 전체 구조에 영향을 주지는 않는다. (※ 표현 방식이 무의미하다는 의미는 아니며, 단지 본 구조의 논의 수준에서는 직접적인 영향이 없다는 뜻이다.)

---

#### MM 내 정보의 태그 지정 및 멀티모달 매칭

각 생성 네트워크(generative network)로부터 들어온 정보는 MM에 저장될 때, 해당 정보가 **어떤 네트워크에서 유래했는지(origin network)**를 **태그(tag)**로 함께 기록한다 (예: 시각 네트워크, 감정 네트워크 등).

그림자 생산 시스템은 이 태그들을 기준으로 정보를 **매칭(match)**하지만, **특정 네트워크에만 국한되지는 않는다.**
예를 들어, **시각 그림자 생산 시스템**은 **감정(emotion)** 및 **시각(vision)** 관련 출력을 모두 참조할 수 있도록 구현할 수 있다(예: 무서운 동물). 이는 실제 인간 인지에서 **한 양상(modality)**이 다른 양상에 영향을 주는 현상을 설명할 수 있게 해준다.

그림자 생산은 또한 WM 내 요소와 MM 내의 **그래프 정보(graph structure)**를 함께 참조하여 매칭할 수 있다. 종합적으로 보면, 그림자 생산 시스템의 주요 기능은 다음 조건 하에서 **최적의 생산을 선택(select the best production)**하는 것이다:

1. 현재 초점(current focus)
2. 과제의 표현(representation of the task)
3. 생성 네트워크들의 예측(predictions of all the networks)

각 그림자 생산 시스템은 **특정 양상(modality)의 전문가(expert)**로서 작동하지만, **다른 정보도 함께 고려하여(contextualize)** 최종 출력을 도출한다.

---

#### WM 버퍼의 통제와 다중 버퍼 구조

작업 기억(WM) 내의 모든 정보는 **해당 정보를 전달한 그림자 생산 시스템**이 해당 정보를 버퍼에 넣는 방식으로 저장된다.
중요한 점은, **각 그림자 생산 시스템마다 자체 버퍼가 존재**하기 때문에, 서로 충돌(conflict)이 발생하지 않는다는 것이다.

따라서, 그림자 생산의 기능은 **WM에 들어가기 전에 정보를 정제하거나 조정(refine/customize)**하는 과정이라고 이해할 수 있다.

---

#### 질의 처리 및 하향식 통제

중심 생산 시스템(main production system)이 정보를 요청할 경우, 해당 **질의(query)**는 **WM 내 관련 버퍼에 삽입**된다.
그림자 생산은 이 질의를 감지하고, **MM에 목표 정보가 존재하는지 여부**에 따라 반응한다.

하지만, **질의는 직접 생성 네트워크에 전달되지 않는다.** 대신, 우리는 다음과 같은 절차를 제안한다:

* **WM의 내용**과 **MM의 내용(활성도에 따라 가중치가 부여된)**을 결합하여,
* 하나의 **대규모 벡터(single, large vector)**로 구성하고,
* 이를 **중심 생산 시스템의 각 주기(cycle)**마다 **모든 생성 네트워크의 입력으로 전달**한다.

그림 Figure 4는 이 구조를 **“문맥(context)”과 “주의(attention)”**로 표시하여 시각화한 것이다. 핵심은, **생성 네트워크가 어떤 정보가 요구될지를 사전에 예측하여 제공하도록 하는 것**이다.

---

#### 절차 기억의 학습과 그림자 생산의 생성

**공통 인지 모델(CMC)**에서 **절차 기억(Procedural Memory, PM)**을 구현하는 **생산 시스템(production system)**은 일반적으로 **시간 지연 학습 알고리즘(Time Delayed, TD learning algorithm)**을 사용하여, **보상(reward)** 또는 **처벌(punishment)**을 야기한 생산 규칙의 **효용값(utility)**을 조정한다.

본 논문에서 제안하는 것은, **모든 모듈에 대해 생산 시스템을 사용함으로써**, 이들 역시 **동일한 TD 학습 메커니즘** 내에 포함시킬 수 있다는 점이다. 구체적으로는 다음과 같다:

* 중심 생산 시스템이 **보상을 획득**할 경우,
* 해당 보상에 **기여(contribute)**한 그림자 생산 시스템들도
* 자신이 WM에 전달한 정보가 **사용되었다면**, **그 효용값을 함께 향상시킨다(boost utility)**.

---

#### 그림자 생산 규칙은 어떻게 생성되는가?

더 어려운 문제는, 바로 **그림자 생산 규칙을 어떻게 생성할 것인가?** 이다.
우리는 이 문제에 대해, **Clarion 아키텍처(Sun 2017)**와 유사한 접근을 제안한다.

* 중간 기억(MM) 내에 **매우 높은 활성값(high activation)**을 가지는 정보가 존재하면,
* 이를 **검색하기 위한 생산 규칙**이 생성된다.
* 해당 생산 규칙은 이후 **보상(reward)**을 받게 되면,
* **영구적인 규칙(permanent production)**으로 **정착(compiled)**되며,
* 그 **효용값이 상승(utility is boosted)**한다.
  → 이는 **ACT-R의 생산 규칙 컴파일(process of production compilation)**과 유사하다.

이와 같은 절차는 일반적인 틀이며, **구체적인 구현 방식은 다양할 수 있다.**
그러나 우리의 핵심 주장은 다음과 같다:

> **모든 모듈을 단일 학습 알고리즘으로 통합하면(coupling all modules under one learning algorithm), 인지 시스템 전반에 걸쳐 학습 효율성 및 적응성이 향상될 수 있다.**

---

### 결론 (Conclusions)

인간은 **매우 적은 반복(few repetitions)**만으로도 규칙을 학습할 수 있는 반면, **신경망(neural networks)**은 **매우 많은 반복(a great many repetitions)**을 통해서야 규칙을 학습한다.
또한, 신경망이 학습한 규칙은 **치명적 간섭(catastrophic interference)**에 취약할 수 있는데, 이는 인간 학습에서는 나타나지 않는 현상이다.

인간은 규칙의 **적용을 잊을 수는 있어도**, **새로운 규칙을 학습함으로써 기존의 규칙이 사라지거나 변형되는 일은 거의 없다.**
이러한 관찰은 인간의 규칙 학습 시스템이 신경 기반(neural)이라는 점은 분명하지만, **인지(cognition)**를 지원하기 위해 다음과 같은 **특수한 구조(specialized structure)**를 포함하고 있음을 시사한다.

예컨대 다음의 뇌 구조들이 그러하다:

* **기저핵(basal ganglia)**
* **해마(hippocampus)**

공통 인지 모델(CMC)에서는, **절차 기억(procedural memory)**이 **기저핵**에 해당하는 것으로 간주되며(Stewart, Choo, and Eliasmith 2010; Stocco et al. 2021),
**중간 기억(Middle Memory)**은 **시상(thalamus)**의 활동과 연관될 가능성이 있다고 본다.

---

이러한 논의는 현재 인공지능(AI) 연구 내에서 다음과 같은 중요한 분기점을 시사한다:

* **생성 네트워크 내부에서의 자발적(emergent) 구조**만으로도 **인간 수준의 지능(human-level intelligence)**을 구현할 수 있는가?
* 아니면, **공통 인지 모델(CMC)**과 같은 **구조적 제약(structural constraints)**이 반드시 필요할까?

본 논문은 **후자의 입장**을 지지한다. 즉, **생성 네트워크를 CMC(또는 유사한 아키텍처)**에 연결함으로써, **통계적/연합 학습(statistical/associative learning)**에서 **고차원적 추론 및 추상화(reasoning and abstraction)**로의 확장이 가능해진다고 본다.

---

### 적용 예시 1: 인과 추론 (Causal Reasoning)

**인과 추론(causal reasoning)**은 다음과 같은 요소로부터 **인과성(causality)**을 추론하는 과정이다(Pearl 2009):

* **통계적 연관(statistical association)**의 존재 및 부재
* 그 조건(conditions)
* 그 결과(outcomes)

**인과 추론**은 **맥락 간 학습 일반화(generalization across contexts)**를 위해 중요하며, **인간 수준의 지능(human-level intelligence)**을 위한 **전제 조건(precondition)**일 수 있다(Juliani et al. 2022).
중요하게도, 인과 추론은 다음 두 요소가 모두 요구된다:

1. **연합 기반 예측(associative prediction)**
2. **체계적인 기호 기반 사고(systematic symbolic thought)**

CMC 기반 아키텍처는 이 두 가지 요소를 모두 아우를 수 있다.

---

### 적용 예시 2: 메타인지 (Metacognition)

**그림자 생산 시스템(shadow production system)**은 **메타인지 과정(metacognitive processes)**도 수용할 수 있다(Conway-Smith and West 2023; Conway-Smith, West, and Mylopoulos 2023).

* 중심 생산 시스템의 활동 요약(summary of central production activity)은
* 그림자 생산 시스템으로 전달될 수 있으며,
* 이는 **모델의 상태에 대한 서사적 정보(narrative-like information)**를 형성한다.
* 이를 통해, 그림자 생산은 **새로운 목표(new goals)**를 중심 생산 시스템에 제안할 수 있다.

이 구조는 메타인지 시스템이 **다른 그림자 생산 시스템의 내부 상태**에 대해 **제한된 지식(limited knowledge)**만을 갖도록 만들 수 있으므로, **자기 참조(self-referential)**와 **자동화된 인지(automated cognition)** 간의 구분을 형성할 수 있다.

---

### 적용 예시 3: 맥락 기반 전문성 (Context-Sensitive Expertise)

보다 일반적으로, 이 시스템은 **복잡한 전문성(complex forms of expertise)**을 모델링하는 데 유용할 수 있다. 이 경우 **맥락(context)**이 매우 중요하며, 그림자 생산은 다음과 같은 역할을 수행할 수 있다:

* **예상치 못한 생성 네트워크의 예측(prediction)**을 감지하고
* **중심 생산 시스템에 경고나 주의 메시지(alarm or cautionary note)**를 보냄으로써
* 시스템이 더 신중하게 행동하도록 유도할 수 있다(West and Nagy 2007).

---

### 벡터 기반 구현과 의미

**홀로그램 벡터(holographic vectors)**는 **기호(symbolic)**와 **연결주의(connectionist)** 처리 방식 모두의 특성을 갖추고 있으며, 다음과 같은 이점을 가진다:

* **생산 시스템에서 사용되는 기호들을, 신경 활동과 유사한 방식으로 구현** 가능
* 예: Kelly 외의 **홀로그램 명시적 기억(Holographic Declarative Memory, HDM)**은

  * 저장된 패턴 위에 **논리 연산자(logical connectives)**를 적용할 수 있는 **대수적 문법(algebraic syntax)**을 제공함
* **망각이나 간섭 현상(catastrophic interference)**으로부터 **벡터 표현을 보호**하는 역할도 가능(Cheung et al. 2019; Mannering and Jones 2021)

따라서, CMC를 **전적으로 벡터 표현(vector representations)**만으로 구성하는 것도 가능하며, 이는 **생성 네트워크와의 연결성** 측면에서 매우 유리하다.

---

### 최종 정리

본 논문이 제안한 프레임워크를 **공통 인지 모델(Common Model of Cognition)**에 통합함으로써, **인지 아키텍처(cognitive architectures)**와 **생성 네트워크(generative networks)**를 이론적·실용적으로 연결할 수 있으며,
이를 통해 **컴퓨터로 모델링 가능한 인간 행동의 범위**를 크게 확장시킬 수 있다.

**예측 처리(predictive processing)**와 **기호 기반 추론(symbolic reasoning)**을, **다중 양상(multimodal)**으로 연결된 CMC 내에서 통합함으로써, 우리는 **AI 분야의 지속적인 난제(persistently unresolved issues)**를 해결하기 위한 **혁신적 접근 방식**을 제시하였다.
