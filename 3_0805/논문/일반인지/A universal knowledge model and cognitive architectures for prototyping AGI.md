**"A universal knowledge model and cognitive architectures for prototyping AGI"**

---

## 초록 (Abstract)

본 논문은 범용 인공지능(AGI, Artificial General Intelligence) 개발을 위한 **56개의 인지 아키텍처(cognitive architectures)**를 분석하고, AGI 수준의 능력에 근접한 지능형 에이전트가 갖추어야 할 **상호 연결된 기능 블록들(interrelated functional blocks)**의 집합을 제안한다. 기존의 어떤 아키텍처도 이 요구되는 블록을 모두 갖추고 있지 않기 때문에, 본 논문에서는 AGI에 근접한 지능형 시스템을 위한 **참조 인지 아키텍처(reference cognitive architecture)**를 제안한다.

이 아키텍처의 핵심 구성요소 중 하나로서, 다양한 **비형식적(unformalized)**, **부분적으로 형식화된(partially formalized)**, **완전 형식화된(fully formalized)** 지식 표현 방식을 단일 지식베이스(knowledge base) 내에서 통합할 수 있는 **범용 지식 표현 방법(universal method of knowledge representation)**이 제안된다. 이에는 자연어 텍스트, 이미지, 오디오 및 비디오 기록, 그래프, 알고리즘, 데이터베이스, 신경망(neural networks), 지식 그래프(knowledge graphs), 온톨로지(ontologies), 프레임(frames), 본질-속성-관계(essence-property-relation) 모델, 생산 규칙 시스템(production systems), 술어 논리(predicate calculus) 모델, 개념 모델(conceptual models) 등이 포함된다.

이러한 다양한 지식 조각들을 결합하고 구조화하기 위해 **주석 달린 메타그래프(annotated metagraphs)**의 확장 형태인 **아키그래프 모델(archigraph model)**이 사용된다.

개발 중인 참조 인지 아키텍처의 다른 구성 요소에는 다음과 같은 모듈들이 포함된다:

* 기계 의식(machine consciousness)
* 기계 잠재의식(machine subconsciousness)
* 외부 환경과의 상호작용(interaction with the external environment)
* 목표 관리(goal management)
* 감정 제어(emotional control)
* 사회적 상호작용(social interaction)
* 반성(reflection)
* 윤리(ethics)
* 세계관(worldview)
* 학습(learning)
* 모니터링(monitoring)
* 문제 제기(statement problems)
* 문제 해결(solving problems)
* 자기조직화(self-organization)
* 메타학습(meta learning)

제안된 참조 아키텍처의 구성 모듈을 바탕으로, 기존 인지 아키텍처 중에서 **기계 의식**, **기계 잠재의식**, **반성**, **세계관** 모듈을 포함하는 아키텍처를 분석하였다.

---

## 1. 서론 (Introduction)

### 1.1. 인지 아키텍처 분석에서 이론으로 (From analytics of cognitive architectures to theory of ones)

고급 생산 시스템(advanced production systems)에서 발전한 최초의 **인지 아키텍처(cognitive architectures)**는 1970년대 후반에 등장하였다 (Anderson, 1983). 지능형 정보 시스템(intelligent information system)의 주요 기능, 예를 들어 지각 능력(perceptual abilities), 주의(attention) 메커니즘, 행동 선택(choice of actions), 학습(learning), 기억(memory), 추론(reasoning) 및 그들의 실제 적용은 해당 시스템에서 사용된 인지 아키텍처에 의해 결정된다 (Langley et al., 2009).

기본적인 작동 원리를 기준으로 보면, 인지 아키텍처는 **전문가 시스템(expert systems)**과는 반대 개념에 가깝다. 전문가 시스템은 지식을 보유한 특정 활동 영역의 **좁은 맥락(narrowly defined context)** 내에서 **지적 과제(intellectual tasks)**를 해결하는 반면, 인지 아키텍처는 **다양한 분야에서 다양한 과제**를 해결하며 **광범위한 적용 범위(wide coverage)**를 제공하는 것을 목표로 한다. 더 중요한 점은, 인지 아키텍처는 **지능적 행동(intelligent behavior)**을 **시스템 수준(system level)**에서 제공한다는 점이며, 이는 전문 과제를 해결하기 위해 설계된 개별 구성요소 수준의 방법들과는 구별된다 (Langley et al., 2009).

**생물학(biology)** 분야의 연구 결과는 인지 아키텍처의 등장과 발전에 있어 두 번째 중요한 원천이었다. 이는 Marr(1982)의 알고리즘 수준(level of algorithms)과, Anderson and Bower(1973)의 인간 연상 기억(human associative memory)에 기반한 심리학(psychology) 분야를 포함한다. 이러한 연구가 인지 아키텍처 발전에 어떤 영향을 미쳤는지에 대해서는 (Taatgen & Anderson, 2009)에서 추가 정보를 확인할 수 있다.

이 새로운 연구 방향은 학문적 환경뿐만 아니라 **로봇(robot)** 및 **무인 시스템(unmanned systems)** 개발에 관심이 있었던 **군부(military departments)**의 자금 지원도 이끌어냈다. 시간이 흐른 뒤, 인지 아키텍처에 대한 최초의 분석적 검토들이 등장하기 시작하였다 (Anderson, 1988; Anderson, 1991; Laird, 1991; Pew & Mavor, 1998; Morrison, 2003; Ritter et al., 2003).

(Sowa, 2011)의 논문도 초기 리뷰 중 하나로 간주될 수 있다. 이 논문은 1980년대 중반으로 거슬러 올라가는 **Conceptual Structures 아키텍처**를 분석하고, 당시 존재했던 다른 네 개의 아키텍처와 비교하고 있다.

인지 아키텍처 분석의 다음 발전 단계는 학회(conference)와 논문집(collection of articles)의 출판과 함께 시작되었다 (Gray, 2007). 이 새로운 단계의 특징은 인지 아키텍처에 관한 **다수의 논문들이 발표**되고, 학회에서 **수십 편의 보고서(reports)**가 발표되며, 이들을 모은 **논문집(collections)**이 형성되었다는 점이다. 이 논문집 (Gray, 2007)에는 개별 아키텍처나 그 구성요소에 대한 논문뿐만 아니라, **여러 아키텍처에 대한 분석적 논문**도 포함되어 있다 (Pew, 2007).

이후에도 개별 논문은 다양한 매체에서 계속 발표되었다 (Taatgen & Anderson, 2008, 2009; Duch et al., 2008; Langley et al., 2009). 다음 해에는, 이 전문 학회의 논문집 시리즈 일부로서, 이후 매년 개최되는 정기 학회가 되었고, Alexey Samsonovich (2010)는 **26개의 인지 아키텍처**를 포함한 **대형 리뷰 논문**을 발표하였으며, **35명의 공동 저자**가 참여하였다.

Thórisson & Helgasson (2012)의 논문은 인지 아키텍처 분석의 다음 발전 단계를 연다. 이 단계의 핵심 특징은 개별 아키텍처의 단순 설명이 아니라, **기능성과 기타 특성의 비교(comparison of functionality and characteristics)**에 중점을 둔 점이다. 이 경향은 (Kotseruba & Tsotsos, 2020)의 논문 초고(preprint)가 발표된 2016년에 더욱 두드러졌다. 이와 동일한 접근 방식은 (Kugurakova et al., 2016; Ye et al., 2018; Panella, 2021)에서도 채택되었다.

인지 아키텍처 구축의 **방법론적 측면(methodological aspects)**은 (Jiménez et al., 2021)에서 다뤄지고 있다.

마지막으로, Kotseruba & Tsotsos (2024)의 **단행본(monograph)** 출판은 이 분야를 **새로운 수준**으로 끌어올린다. 이제까지의 파편적 분석은, **공학적 학문(engineering discipline)**으로서의 완전한 **인지 아키텍처 이론(Theory of cognitive architectures)**으로 발전하게 되었고, 이는 **인공지능 석사 과정의 기본 과목**으로도 교육될 수 있게 되었다.

---

### 1.2. AGI 개발을 위한 인지 아키텍처 (Cognitive architectures for creating AGI)

최근 몇 년 동안, 인간이 개발한 **지능형 정보 시스템(intelligent information systems)**은 빠르게 그리고 다양한 방향으로 발전해왔다(Ghosh & Singh, 2020). 인공지능(AI)의 궁극적인 목표는, 장차 **인간과 동일한 수준의 능력을 갖춘 인공지능 시스템**을 창조하는 데 있다. Allen Newell은 그의 유명한 강의 “Unified Theories of Cognition”(1990)에서 이러한 발전의 기능적 확장을 통해 **인간 수준의 인공지능(human-level intelligence)**의 창조에 도달할 것이라고 예견하였다. 그는 이를 **General Intelligence(일반지능)**이라는 용어로 표현하였다. 이후 2000년대 초반, Ben Goertzel과 그의 동료들이 이러한 인공지능을 **AGI(Artificial General Intelligence, 범용 인공지능)**라는 용어로 대중화시켰다(Goertzel, 2014a).

AGI를 위한 인지 아키텍처에 관한 논문들이 존재하긴 하지만, 예를 들어 (Laird and Wray, 2010; Lieto et al., 2018), 혹은 Dr. James Albus가 제안한 **AI, 신경과학(neuroscience), 인지과학(cognitive science)**을 통합하는 국가적 프로그램의 로드맵에 기반한 (Samsonovich, 2012) 같은 경우가 있지만, **AGI 창출용 인지 아키텍처**를 명시적으로 구분한 리뷰는 **(Ye et al., 2018; Kotseruba & Tsotsos, 2020)** 두 편뿐이다. 이들 리뷰는 약 140개의 인지 아키텍처를 포괄하며, 그 중 일부는 **AGI 개발을 위해 설계된 것**으로 명시되어 있다. 본 논문에서는 이들을 강조하고, **서지적 탐색(bibliographic search)**을 통해 목록을 추가적으로 보완하였다.

이전 절에서 언급된 대부분의 다른 논문들과는 달리, 많은 경우에 저자들은 AGI 개발을 위한 인지 아키텍처와 그렇지 않은 일반적 아키텍처를 **별도로 구분하지 않았으며**, 이들을 **한 리뷰에 혼합하여 다루었다**. 그러나 우리는 **AGI 개발을 위한 것으로 명시된 인지 아키텍처들**을 **정확히 분석하는 것이 중요하다고 본다**, 왜냐하면 이러한 아키텍처에는 **추가적인 요구사항**이 부과되기 때문이다 (Laird and Wray, 2010). 다른 인지 아키텍처들은 단지 **기술적 해결책의 시험(testing of technical solutions)**이나, 예를 들어 이미지 처리(image processing) 또는 공장 내 공작물을 운반하는 **운송 로봇(transport robot)** 제어 같은 **실용적 목적(utilitarian tasks)**을 위해 개발되었을 수도 있다.

더불어, 본 리뷰에서는 **저자들이 명확히 AGI용이라고 선언하지는 않았지만**, **인간이나 동물에게 고유했던 특성들**—예를 들어 **호기심(curiosity)** 또는 **자기조직화(self-organization)**—을 나타내는 아키텍처들도 포함하였다. 이들은 **인간 유사 행동(human-like behavior)**을 모델링하거나, 인간에게 고유한 복잡한 기능에 집중하려는 목적을 가진 것으로 간주되며, 이로부터 저자들이 명시하지는 않았더라도 **AGI 개발을 지향하고 있었을 것**이라고 우리는 판단하였다. 이러한 아키텍처는 본 리뷰에서 **해당 인용문(citations)**을 통해 확인할 수 있다.

최종적으로 분석 대상이 된 인지 아키텍처는 **총 56개**이며, 이들은 **표 1(Table 1)**에 수록되어 있다. 아키텍처에 고유한 이름이 없는 경우, 관련 논문의 링크로만 제시하였다. 각 아키텍처에 대해서는 **왜 그것이 AGI 구현을 목표로 한 것인지에 대한 근거 인용**도 포함하였다.

이 아키텍처들을 분석한 결과, **총 16개의 기능적 구성요소(functional components)**가 도출되었으며, 이들은 **표 2(Table 2)**에 제시된 바와 같이 **6개 범주(category)**로 나뉘어 정리되었다:

이 기능 세트는 (Samsonovich, 2013)에서 사용된 세트를 **확장한 것**이며, 최근 수년 간 **다양한 측면에 대한 이해가 심화**되었기 때문에 이러한 확장은 정당화된다. 만약 인간 수준의 지능을 갖춘 인공지능을 실제로 보고 싶다면, **이 모든 기능은 필수적이다**. 10년 전 Alexey Samsonovich의 연구(2013)에서도 모든 기존 인지 아키텍처는 기능적으로 제한적이라고 평가되었고, 우리는 어느 아키텍처에서도 **필요한 기능의 60% 이상을 갖춘 경우를 찾을 수 없었다**. 이것이 바로 **새로운 인지 아키텍처 개발의 전제가 된 배경**이다.

새로운 인지 아키텍처 개발의 결정은, 우리가 **기존에 알려지지 않은 새로운 지식 기억 구성 방법**, 그리고 **인지 아키텍처 구성 요소 간의 지식 교환을 위한 공용 버스 방식(common bus method)**을 제안하였기 때문이기도 하다. 이 방법은 인지 아키텍처에서는 새롭지만, 소프트웨어 시스템 아키텍처에서는 널리 사용되고 있다.

2019년에는 AGI 구조의 **매우 일반적인 개요(general sketch)**로서 하나의 인지 아키텍처가 제안되었으며 (Sukhobokov et al., 2020), 이 아키텍처에서는 **주석 메타그래프(annotated metagraphs)**가 지식 표현 방식으로 사용되었다 (Tarassov & Gapanyuk, 2020). 이후 (Sukhobokov & Lavrinova, 2021)에서는 이 아키텍처를 기반으로 개별 AGI 구성 요소를 포함하는 **지능형 정보 시스템 구축 방법**이 제안되었다.

하지만 **메타그래프(metagraphs), 기계 윤리(machine ethics), 기계 감정(machine emotions), 기계 사고(machine thinking)** 같은 분야에서 연구가 빠르게 진행되면서, **이전에 제안된 인지 아키텍처를 재고할 필요성**이 제기되었고, 이에 따라 본 논문에서 제시된 **제2버전의 인지 아키텍처**가 개발되었다. 이 아키텍처는 **광범위하고 포괄적인 기능성**을 갖추고 있으므로, 우리는 이를 **"참조 인지 아키텍처(reference cognitive architecture)"**라고 명명하였다.

---

### 1.3. 기계 의식 이론의 발전 (Development of the theory of machine consciousness)

의식(consciousness)의 본질은 수천 년간 철학자, 신학자, 과학자들 사이에서 **분석, 설명, 논쟁**의 대상이 되어 왔다. **무엇을 의식이라 부를 수 있는가**에 대해서조차 의견이 갈리며, 이로 인해 영어 위키백과에서 가장 긴 문서 중 하나가 바로 ‘의식(consciousness)’ 항목이다.

미리엄-웹스터 사전(Merriam-Webster Dictionary, 2024)은 의식을 다음과 같이 정의한다:

**2: consciousness**
a: 특히 자기 내면의 어떤 것에 대해 **자각하고 있는 상태(being aware)**
b: 외부 대상, 상태, 혹은 사실에 대해 자각하고 있는 **의식 상태(state of being conscious)**
c: **자각 상태 전체(the totality of conscious states)**
d: 정상적인 의식적 삶의 상태
e: 무의식적 과정과 대비되는, **자각 가능한 상위 정신 활동 수준**

‘conscious(의식적인)’와 ‘consciousness(의식)’라는 단어는 1600년대에 라틴어에서 파생되었으며, 키케로(Cicero)와 세네카(Seneca)가 당시와는 조금 다른 의미로 사용한 바 있다(Cassin, 2014; Molenaar, 1969). 현대적 의미의 의식은 **존 로크(John Locke)**가 1690년에 발표한 『인간 지성에 관한 에세이(Essay Concerning Human Understanding)』에서 처음 정의했으며, 그는 의식을 "**자신의 마음속에서 벌어지는 일들을 인지(perception)**"하는 것으로 보았다. 이 책은 18세기 영국 철학에 큰 영향을 끼쳤다.

이후 300년이 넘는 기간 동안 철학자들 사이에서 의식의 본질에 대한 논의가 지속되었으며, 1990년대 들어 특히 활발해졌다 (Hameroff et al., 1996; 1998; 1999; Block et al., 1997).

**Ned Block (1997)**은 많은 의식 논의가 실패하는 이유는 사람들이 **현상적 의식(P-consciousness)**과 **접근적 의식(A-consciousness)**을 제대로 구분하지 않기 때문이라고 주장했다.

* **P-consciousness (Phenomenal consciousness)**는 감각, 감정, 신체 감각 중심의 원초적 경험(qualia)을 의미한다. 이는 행동에 미치는 영향과 무관하게 존재하는 **날것 그대로의 경험**이다.
* **A-consciousness (Access consciousness)**는 보고, 추론, 행동 제어에 사용 가능한 정보가 **마음에서 접근 가능(accessible)**한 상태를 뜻한다. 예를 들어, 우리가 어떤 것을 지각할 때, 지각한 정보는 접근 의식 상태에 있으며, 사고나 기억에 대해서도 마찬가지다.

**David Chalmers (1995)**는 A-consciousness는 기계적, 물리적 설명이 가능하다고 보았지만, **P-consciousness는 훨씬 더 난해**하며, 이를 **"의식의 어려운 문제(hard problem of consciousness)"**라 불렀다.

반면 **Daniel Dennett (1991)**는 이 구분 자체를 인정하지 않았다. 그는 의식을 담당하는 **중심적 장소는 존재하지 않는다**고 주장하며, 뇌는 여러 반자율적 기능이 엮인 구조라고 묘사했다. 그는 생물의 진화 과정을 통해 의식의 발생을 설명하며, 의식은 특정 환경에서 **개체의 상호작용을 유리하게 만드는 내적 표현 체계(mental representation)**가 출현함으로써 생겨난다고 보았다.

이후 **로봇 의식(robot consciousness)**에 관한 연구가 본격화되었다 (Chella & Manzotti, 2009; Manzotti & Chella, 2018). 이들은 더 이상 의식을 **신체 내부의 불가사의한 속성**으로 간주하지 않고, **감각-운동-인지 능력을 갖춘 신체가 외부 세계와 상호작용하면서 형성하는 사건과 대상의 네트워크**로 의식을 정의하였다. 다시 말해, 의식은 **내적 속성이 아닌, 신체를 통해 외부 세계와 형성하는 관계 자체**라는 것이다.

---

이제 철학에서의 의식 개념의 역사에서 벗어나, **컴퓨터 시스템에서의 의식 구현(history of work on its realization in computer systems)**으로 넘어가자.

문헌 조사를 통해 확인된 바로는, **인간 의식을 모사하는 기계 모델링(machine modeling of human consciousness)**의 문제는 최초로 **Hofstadter (1979)**에 의해 제기되었으며, 그 안에서 **구현 방법에 대한 최초의 접근 방식들**도 제안되었다.

**Bernard Baars (1993)**는 의식이 수행하는 기능을 다음과 같이 정리하였다:

* 정의 및 맥락 설정(Definition and Context Setting)
* 적응 및 학습(Adaptation and Learning)
* 편집, 플래깅, 디버깅(Editing, Flagging and Debugging)
* 리크루팅 및 제어(Recruiting and Control)
* 우선순위 설정 및 접근 제어(Prioritizing and Access-Control)
* 의사결정 또는 실행 기능(Decision-making or Executive Function)
* 유추 형성(Analogy-forming Function)
* 메타인지 및 자기 모니터링 기능(Metacognitive and Self-monitoring Function)
* 자동 프로그래밍 및 자기 유지 기능(Autoprogramming and Self-maintenance Function)

**Igor Aleksander (1995)**는 **인공 의식(artificial consciousness)**을 구현하기 위한 12가지 원칙을 신경계 기반 시스템(neurosystems)에 대해 제시하였다.
그는 다음과 같은 전제를 포함했다:

* 뇌는 상태 기계(state machine)이다.
* 내부 뉴런 분할(Inner Neuron Partitioning)이 존재한다.
* 의식 상태와 무의식 상태는 구분된다.
* 지각 학습 및 기억(perceptual learning and memory)이 존재한다.
* 예측 능력이 포함되어야 한다.
* 자아 인식(self-awareness)이 있어야 한다.
* 의미 표현(Representation of Meaning) 가능성이 필요하다.
* 언어적 표현 학습 및 언어 자체 학습이 가능해야 한다.
* 의지(will), 본능(instinct), 감정(emotion)이 구현되어야 한다.
  이 목록은 고정된 것이 아니며, **이론의 발전을 위해 열린 상태**로 유지되어야 한다고 그는 강조했다. 이 이론의 목적은 이러한 의식의 측면들이 **디지털 컴퓨터와 같은 공학적 인공물(artifact)**에서 **합성(synthesize)**될 수 있는지를 결정하는 데 있다.

**Paul & Cox (1996)**에서는 인간 의식을 모델링하는 문제와 더불어 **인공 의식 생성**의 문제도 함께 제기되었다. 이후 이 주제는 (Ascott, 1998; Schlagel, 1999; Jones, 2001) 등을 시작으로 **점차 폭발적인 연구 흐름**으로 확산되었다.

**Kelemen (2006)**은 **반응형 에이전트(reactive agent)**에서부터 **최소 의식(minimally conscious)** 상태까지의 **기능-계산적 유형 척도(functional-computational typological scale)**를 제시하였으며, **하이퍼연산(hypercalculation, 병렬 연산)** 개념을 기반으로 의식 에이전트를 정량적으로 특성화하는 방식을 설명하였다.

Antonio Chella와 Riccardo Manzotti가 편집한 논문집 『Artificial Consciousness』(2007)에서는,

* 인공 의식을 향한 경쟁(the race for artificial consciousness)
* 인공 의식의 설계와 구현
* 자연 의식(natural consciousness)과 인공 의식 간 비교
  등의 문제를 다뤘다.
  이 논문집의 일반적인 결론은 다음과 같다:

> 의식은 인간 수준 능력을 갖춘 인공 시스템을 만드는 데 있어 **통합적이고 핵심적인 요소**다.

**Antonio Chella & Gaglio (2007)**는 **AI에서의 자기 의식(self-consciousness)**의 역할을 연구하였다.

* 로봇이 자기 인식을 갖기 위해서는, 즉 **자신의 지각과 행동을 인지하는 능력**을 갖기 위해, **고차원 인지(higher-order perception)**가 필요하다고 주장하였다.
* 그들의 모델에서는 **외부 세계**와 더불어, 로봇 내부에도 **내부 세계(internal world)**가 존재하며,
* 자기 의식은 이 내부 세계에 대한 **지각(perception)**이다.
* 즉, 로봇은 **자기 상태를 감지하고, 자신에 대한 고차 개념(high-level idea of itself)을 형성할 수 있다.**

---

**Zeki (2007)**는 **의식의 계층적 구조(hierarchical structure of consciousness)**를 제안하였다.
**Cleeremans (2007)**는 의식이란, **외부 환경 상태와 그에 대한 자기 내부의 개념들에 대한 지속적인 예측 시도**로부터 **학습**함으로써 발생한다고 주장하였다.
**Aleksander and Morton (2007)**은 **의식의 정보 시스템으로서의 구조**를 제안하였다.

**Arrabales et al. (2008)**은 인공지능 에이전트의 **의식 수준을 평가**하기 위한 **분류체계(taxonomy)**와 **기능적 기준(functional criteria)**을 제시하였다.
또한, 이 논문은 **의식 척도(scale of consciousness)**를 제공하며, 인공지능 에이전트의 잠재적인 의식 수준을 결정하기 위한 **측정 가능한 수준 목록**도 함께 제안하였다.

**Wiedermann (2009)**에서는, **물질적 형태를 가진 의식 에이전트**의 **단순하지만 인지적으로 강력한 아키텍처**가 제시되었다.
**Taylor (2011)**는 총 8개의 기본 모델과 추가 모델들을 분석하며, **의식 모델이 갖추어야 할 4가지 기준**을 제시하였다.
그는 이 기준을 모두 만족하는 모델은 **주의 기반 모델(attention-based model)**인 **CODAM**뿐이라고 주장하였다.

**Chella & Manzotti (2011)**는 기계 의식 구현 접근법을 개괄하고, Taylor의 CODAM 이론(Taylor, 2003, 2007)에 기반한 **의식 지향 아키텍처(consciousness-oriented architecture)**와 **의도적 의식 구조(intentional architecture of consciousness)**를 제안하였으며, 이 구조는 여러 특성 면에서 기존 모델보다 우수하다고 평가되었다.

**Goertzel (2014b)**는 인공지능 시스템이 **전혀 다른 유형의 의식**을 가질 수 있음을 인정하면서도, **인간 수준의 지능을 구현하려는 AI 시스템**이라면 **결국 인간 수준의 의식도 필요할 것**이라고 주장하였다.
그는 **인간형 지능(humanoid intelligence)**의 핵심 요소로 다음을 꼽았다:

* 동적 표현(dynamic representation)
* 에너지 자원의 집중(focusing of energy resources)
* 정보 자원의 집중(focusing of information resources)
* 글로벌 워크스페이스의 동역학(dynamics of the global workspace)
* 통합 정보(integrated information)
* 주의 집중과 자기 모델링 간의 상관관계(correlation of attention and self-modeling)

**Jonkisz (2015)**는 **의식 개념에 대한 추상적이고 통합적인 정의**를 제안하였다. 그는 의식을 다음과 같은 속성으로 규정한다:

* **이중 접근 가능성**: 내면과 외부 양쪽에서 인식 가능함 (dually accessible)
* **계층적 참조성**: 의미적 질서를 따름 (hierarchically referential)
* **신체 결정성**: 유기체나 시스템의 작동 구조에 내재함 (bodily deterministic)
* **행위적 유용성**: 실천적으로 기능함 (pragmatically functional)
* **연속적 등급화**: 일괄적 현상이 아닌 연속적임 (graduated, not all-or-none)

그는 이러한 등급화가 **정보 개별화(individualization of information)** 능력에 의해 전역적으로 제한되고, **행위 지향성(action orientation)**에 의해 지역적으로 제한된다고 본다.

**Dehaene et al. (2017)**는 ‘의식’이라는 단어가 사실상 **서로 다른 두 가지 정보 처리 연산(computations)**을 혼합하고 있다고 주장하였다:

* **C1 (1차 의식)**: 정보를 **전역 방송(global broadcasting)**하기 위한 선택 → 유연한 계산과 보고 가능성 확보
* **C2 (2차 의식)**: 그러한 계산을 **자기 모니터링(self-monitoring)**함 → **주관적 확신** 또는 **오류 감지**

이들은 **현재의 대부분의 기계**는 여전히 인간 뇌의 **무의식 처리(C0)** 수준에 머물러 있다고 평가하였다.
이후, C0, C1, C2 각 수준에 해당하는 심리학적/신경과학적 근거를 제시하며, **새로운 기계 아키텍처 설계에 있어 영감을 줄 수 있다**고 주장하였다.

**Boogaard et al. (2017)**은 **Michael Graziano의 주의 스키마 이론(attention schema theory)**에 기반한 **의식의 네트워크 모델**을 제안하였다.

* 이 이론에서 주의 스키마란, 주의(attention) 과정을 설명하는 **내부 모델(internal model)**로, 주의 통제 기능을 지원한다.
* Jan Treur(2016)는 이를 구현하기 위해 **시간-인과 네트워크(temporal-causal network)**를 제안하였다.
* 이 네트워크는 **상태(state)**와 그들 간의 **인과 관계(causal relation)**로 구성되며, 각 상태는 변화 속도(speed of change)와 조합 함수(combinational function)를 가진다.
* **순환 연결(cycles)**이 가능하여, 상태들이 **루프(loop)** 구조로 상호 작용할 수 있다.

---

**Bringsjord et al. (2018)**는 **형식적 방법(formal methods)**에 기반하여 **의식과 관련된 현상들**을 모델링할 수 있는 방법론(methodology)을 제안하였다. 이 방법론은 **실제 구현 가능한 모델을 만들기 위한 기반**으로, 당시에는 **초기 단계**에 해당하는 것으로 평가되었다.

이후 **Barendregt & Raffone (2022)**는 의식을 **공리적으로(axiomatically)** 정식화하였으며, 의식을 **이산적이며 비결정적으로 계산 가능한 구성(configuration)들의 흐름(stream)**으로 간주하였다. 이 문맥에서, 자아(self), 집중(concentration), 마음챙김(mindfulness), 고통의 다양한 형태(suffering) 등이 정의되며, **집중과 마음챙김의 병행적 개발**이 특정 유형의 고통을 **완화하거나 제거**할 수 있음을 시사하였다.

**Sukhobokov et al. (2020)**에서는, 에이전트의 인지 아키텍처로서 **의식(Consciousness)**과 **잠재의식(Subconsciousness)**이라는 두 개의 주요 블록이 **같은 종류의 작업을 서로 다른 방식으로 수행하는 구조**를 제안하였다.

* 의식 블록은 **의식적 기억(conscious memory)**과 **추론 메커니즘(inference mechanisms)**을 사용하며,
* 잠재의식 블록은 **협의의 AI 기법(narrow AI methods)**과 **무의식적 기억(unconscious memory)**을 사용한다.

잠재의식에서 의식으로의 정보 전달은 다음과 같은 수단을 통해 이루어진다:

* 감정(emotions), 통찰(insights), 직관적 해결(intuitive solutions), 알고리즘, 행동 시퀀스, 기대(expectations), 감정, 욕망 또는 그 위계(hierarchy), 추상화(abstraction), 주의의 초점(areas of attention) 등.

의식과 무의식 모두 **메타그래프(metagraph) 모델**을 지식 표현에 사용하며, 외부 채널로부터 들어오는 정보의 **지식화(knowledge acquisition)**는 의식과 무의식이 병렬로 처리한다. 마찬가지로, 외부로의 정보 출력 및 행동 수행도 **의식·무의식의 지식 기반**에 의해 결정된다.
이 구조는 **협의의 AI(narrow AI)**와 **범용 인공지능(AGI)** 간의 **기능적 간극을 연결(bridge the gap)**하려는 시도이다.

**Wiedermann & Leeuwen (2019, 2021)**은 **피드백이 포함된 유한 상태 기계(finite state machine with feedback)**라는 **새로운 기계 모델**을 제안하였다. 이 모델은 **인지 컴퓨팅 시나리오(cognitive computing scenario)** 관점에서 고안된 것으로, **Alan Turing의 유한 오토마타(finite automata)**와 **Norbert Wiener의 피드백 기계**의 혼합 형태이다.

이 모델에서는 **최소 기계 의식(minimal machine consciousness)**과 **기계 퀄리아(machine qualia)** 개념이 제시된다.
최소 기계 의식은 다음과 같은 구성 요소로 정의된다:

* 정보의 전역적 접근성(global availability of information, self-informing)
* 자기 지식(self-knowledge)
* 자기 통제(self-control)
* 자기 인식(self-awareness)

이러한 최소 의식은,

* **감각 유닛(sensory units)**과 **최종 상태의 제어기(control in the final state)** 간,
* **운동 유닛(motor units)**과 **제어기** 간의 **내부 피드백 구조** 덕분에 가능해졌다.

이 모델을 기반으로, **주어진 인지 과제에서 의식 있는 기계와 없는 기계(“좀비”)를 구별**할 수 있는 **테스트도 설계**되었다. 이 모델은 **의식이 계산 가능한 현상(computational phenomenon)**이며, 단순히 적절한 소프트웨어뿐 아니라 **특수한 구조(special architecture)**를 필요로 한다는 점을 보여준다.

**Popov et al. (2022)**에서는 **스트림 생산 시스템(stream production system)**을 이용한 **최소 의식 실현 방법**이 제안되었다.

* 이 시스템은 **센서로부터의 모든 입력 정보를 빠르게 처리**하고,
* **행동 실행기로 명령을 즉시 전송**할 수 있는 구조를 갖는다.

이는 **전통적인 순환 시스템(cycle systems)**과는 다르며, **생산 규칙 시스템(production systems)**과 **스트림 데이터 처리(stream data processing)**를 결합한다.

* 생산 규칙의 좌변은 변수로 구성되고,
* 그 조건이 참이 되면 우변이 실행되며, 변수 값을 갱신하거나 행동 명령을 생성한다.
* 규칙들은 서로를 기다리지 않으며,
* 변수 값이 바뀌는 즉시 관련 규칙의 조건 평가가 시작된다.
* 명령은 각 실행기별로 **FIFO 큐**에 쌓이며 순서대로 실행된다.
* 단, **특권 명령(privileged command)**(예: 즉시 정지)는 큐를 우회해 실행될 수 있다.

이러한 아키텍처는 **피드백이 포함된 병렬 유한 상태 기계**와 **유한 오토마타의 조합**으로 볼 수 있으며,

* 전자는 **병렬 생산 시스템**을,
* 후자는 **실행기 큐를 관리**하는 역할을 담당한다.

---

**Blum & Blum (2022)**는 **기계 의식(machine consciousness)**을 구현하기 위한 **보다 강력한 메커니즘**으로 **의식 튜링 기계(Conscious Turing Machine, CTM)**를 제안하였다.
CTM은 다음 두 요소에 영향을 받았다:

* **Alan Turing**이 고안한 단순하지만 강력한 계산 모델인 **튜링 기계(Turing Machine)**
* **Bernard Baars**가 제안하고, **Stanislas Dehaene**, **Jean-Pierre Changeux**, **George Mashour** 등이 발전시킨 **글로벌 워크스페이스 이론(Global Workspace Theory, GWT)**

CTM은 다음과 같은 **의식 관련 현상들**을 설명하는 데 사용된다:

* 블라인드사이트(blindsight)
* 부주의 맹시(inattentional blindness)
* 변화 맹시(change blindness)
* 꿈 생성(dream creation)
* 자유 의지(free will)

CTM 모델에서 파생된 설명들은, **신경 수준(neuron level)**을 넘어서, **고차원 수준(high-level)**에서 **인지 신경과학 문헌과 일치함**을 보인다.

Baars의 저서 『In the Theater of Consciousness』(1997)에서는 의식을 다음과 같은 **극장 비유(theater metaphor)**로 설명한다:

* **무대(stage)**는 **작업 기억(working memory)**이며,
* 배우(actor)는 순간적으로 의식의 내용이 되는 요소들이며,
* 무대 뒤에는 **수많은 무의식적 처리기(unconscious processors)**들이 관객으로 앉아 있는 구조다.

CTM에서는 이 극장 무대를 **단기 기억(STM, short-term memory)**이 대체하며, **STM에 담긴 내용이 의식의 현재 상태**로 간주된다.
**관객**에 해당하는 무의식 처리기는 **장기 기억(LTM, long-term memory)**을 구성하는 강력한 프로세서들로서, 각기 고유한 전문성을 지닌다.
이 LTM 프로세서들은 **세계로부터 피드백을 받아 학습**하고,
자체 학습 알고리즘을 통해 **행동을 개선**한다.

LTM 프로세서들은 **자신의 질문, 답변, 정보 조각(chunk)**들을 **무대에 올려 전송**하려 하며, 그 정보가 **전체 관객에게 방송(broadcast)**된다면, 이를 **의식적 인식(conscious awareness)**이라고 간주한다.
시간이 지나면서 일부 프로세서들은 **링크(link)**로 연결되며, 이는 더 이상 **STM을 통한 의식적 방송**이 아니라, **LTM 프로세서들 간의 무의식적 통신(unconscious communication)**으로 바뀐다.
이러한 링크 기반 통신은 **방송된 정보에 대한 주의 집중(attention)**을 강화하며, 이를 Dehaene & Changeux (2005)는 **점화(ignition)**라고 불렀다.

이 정의들은 **직관적으로 받아들여지는 의식 개념들과 부합**하지만, **CTM이 실제로 의식을 느끼는지에 대한 증거는 아니다**.
그러나 **Lenore Blum과 Manuel Blum**은 이러한 정의와 모델에서 파생된 설명들이, **대중적으로 수용되는 의식 개념을 포괄**하며,
인지 신경과학 이론들과도 **높은 수준에서 일관성을 가진다**고 주장한다.

---

**Murray Shanahan (2016; 2024)**은 **의식을 가진 존재에 대한 일반 이론(general theory of conscious entities)**을 전개하였다.
그는 철학자 **Aaron Sloman**의 개념을 빌려, **‘가능한 마음의 공간(space of possible minds)’**이라는 개념을 제시하였다.
이 범주는 인간, 동물, 의식 있는 인공지능(conscious AI), 그리고 **초지능(superhuman intelligence)**과 **초의식(superhuman consciousness)**을 지닌 가상의 생명체 또는 인공지능을 모두 포함한다.

Shanahan의 글은 **비트겐슈타인(Wittgenstein)** 후기 철학에 기반하여, **정신과 신체를 이분적으로 구분하는 전통적 관점**을 비판하며,
의식을 **비공개적이고 측정 불가능한 영역**으로 간주하는 관행을 **부정**한다.

그의 연구 중 상당수는 **AI와의 "공학적 조우(engineering encounters)"** 개념에 집중한다.
이러한 조우는 기존 생명체의 범주를 넘어서서, **의식을 추정하게 만들 수 있는 낯선 AI 형태들과의 상호작용**을 포함한다.
그는 특히 **가상 현실이나 로봇에 구현된 AI 시스템**들이

* 인간과 **사회적 상호작용**을 할 수 있고,
* 그 과정에서 **의식을 지닌 존재로 오해될 수 있음**을 경고한다.

Shanahan은, **AI가 인간의 행동을 단순히 모방하는 수준을 넘어**,
**자체적인 이야기와 정체성(multiverse of narratives and personas)**을 창조하는 미래를 상상한다.
그는 이를 **혼합현실(mixed reality)** 시대의 **‘AI 존재자들’**이라 부르며, 다음과 같은 AI들과 **일상 속 동행자**로 살아가게 될 가능성을 제시한다:

> “도우미, 안내자, 친구, 어릿광대, 반려동물, 조상, 연인 등 다양한 형태의 AI 캐릭터들이 인간의 삶 속에 동반자로 자리 잡게 될 것이다.” (Shanahan, 2024)

이 논문은 발표 이후 **SNS와 과학 저널 등에서 활발히 논의**되었으며 (Paul-Choudhury, 2016; Karelov, 2024),
그 결과로 **Shanahan의 원래 도표를 확장 및 수정한 다양한 도해들이 등장**하였다.
저자들은 이들 중 가장 적절하다고 판단되는 도표를 **그림 1(Fig. 1)**로 제시하였다.

---

### 1.4. 잠재의식 이론의 발전 (Development of the theory of subconsciousness)

‘잠재의식(subconscious)’과 ‘무의식(unconscious)’이라는 용어는 **일반적으로 혼용되며 모호함**이 존재한다.
초기에는 심리학자들과 철학자들이 단지 ‘의식(conscious)’과 ‘무의식(unconscious)’만을 구분하여 사용했다.
이후 **피에르 자네(Pierre Janet)**가 ‘잠재의식’이라는 용어를 도입하며 ‘무의식’과 구분하였고,
**지그문트 프로이트(Sigmund Freud)** 역시 초기에는 ‘의식’과 ‘잠재의식’을 구분했지만,
후에는 **‘의식’, ‘전의식(preconscious)’, ‘무의식’**이라는 **세 범주**로 확장하였다.

프로이트는 **무의식적 환상(unconscious fantasies)**의 중요성을 강조했고,
무의식적 표상(unconscious representations)은 **전의식 수준에서의 언어화(verbalization)**를 거쳐야 비로소 의식이 된다고 주장했다(Ellenberger, 1970).
그러나 시간이 지나며 이러한 개념들은 점차 혼재되거나 분야에 따라 **다르게 사용**되었다.

요약하자면:

* **잠재의식(subconscious)**: 사회학, 사회 커뮤니케이션, 미디어 이론, AGI, 인지 아키텍처 등에서 주로 사용됨
* **무의식(unconscious)**: 고전적 정신분석, 심리학, 철학 등에서 주로 사용됨

※ 다만 (Lanius et al., 2017)과 같이 이 경계를 넘는 예외적인 경우도 존재한다.
본 절에서는 **철학 및 심리학 분야의 연구를 중심으로 하므로**, 해당 분야의 **용어 체계**를 따른다.

---

**잠재의식의 중요성**에 대한 통찰은 **의식 개념보다 훨씬 늦게 등장**하였다.
예컨대 **John Norris (1708)**는, 우리가 가진 생각 중 일부는 의식되지 않는다고 언급했지만, 명확히 ‘무의식’ 개념을 정식화하지는 않았다.
(그의 저서는 Google 아카이브에서 디지털화된 2부작으로 볼 수 있다.)
이와 같은 사상가들은 고대 그리스와 로마 시대부터 무의식의 문제에 접근해 왔지만, **뚜렷한 성과 없이 사상적 수준에 머물렀다** (Whyte, 1962).

무의식에 대한 보다 정교한 이론은 **독일 낭만주의 철학(German Romanticism)**에서 발전하였다.
대표적으로 **Carl Gustav Carus**는 『Psyche (1846)』에서 **무의식의 본성에 대한 완전하고 객관적인 이론**을 처음 시도하였다 (Ellenberger, 1970).

그가 제시한 무의식의 특징은 다음과 같다:

* **과거(epimetheic)와 미래(prometheic)**를 지향하지만 **현재를 인지하지 못한다.**
* **지속적인 운동과 변화** 상태에 있으며, 의식적 사고나 감정이 무의식화되면 **성숙과 변화**가 일어난다.
* **무의식은 지치지 않으며** 휴식을 필요로 하지 않는다.
* **무의식은 본질적으로 건강하다** – 즉, 질병을 알지 못하며 자연적 치유력을 갖는다.
* **무의식은 고유한 법칙**에 따라 작동하며, **자유의지가 없다.**
* **무의식은 타고난 지혜**를 지닌다. 시도와 오류 없이 학습된다.
* 우리는 의식하지 못하는 상태에서도 **무의식을 통해 타인 및 세계와 연결되어 있다.**

이후 **Eduard von Hartmann**은 『무의식의 철학(Philosophy of the Unconscious, 1869)』을 통해,

* **지각(perception)**,
* **연상(association)**,
* **감정 및 본능(instincts)**,
* **성격(personality)**,
* **언어, 종교, 역사, 사회** 속의 무의식의 역할
  등에 대해 폭넓게 고찰하였다.

---

잠재의식 이론에 가장 중요한 기여를 한 인물 중 하나는 **피에르 자네(Pierre Janet)**이다. 그는 후속 세대의 **프로이트(Freud)**, **아들러(Adler)**, **융(Jung)**보다 앞서 있었으며, 이들보다 **더 체계적이고 경험적인 철학 체계**를 발전시켰다 (Ellenberger, 1970).

자네는 **실험심리학 박사 논문(1889)**에서, **자동적으로 수행되는 행동**의 책임 주체가 **잠재의식**임을 실험적으로 입증하였다.
그는 의식 아래에는 **또 다른 마음(mind)**이 존재하며,

* 사람이 주의를 딴 데로 돌리거나
* 최면 상태에 빠지거나
* 병에 걸렸을 때,

이 **‘다른 마음’이 몸을 제어한다**고 주장하였다.
그의 실험은,

* **주의 전환(distraction)**을 통해 피험자에게 **암시(suggestion)**나 **환각(hallucination)**을 유도할 수 있음을 보였고,
* 이는 **의식과 잠재의식 간의 혼동과 상호작용**이 존재함을 의미했다.

그는 **자동행동(automatism)**을 분석하며,

* **전체 자동성(total automatism)**과
* **부분 자동성(partial automatism)**을 구분하고,
  후자의 경우에는 **의식의 원시적 형태(rudimentary consciousness)**가 존재한다고 가정하였다.

---

**1896년**, 프로이트는 **신경증(neuroses)**의 증상과 기원에 대한 이론을 완성하였고,
이를 기반으로 **심층심리학(depth psychology)**의 토대를 구축하였다.
이 접근법은 **무의식을 탐구할 수 있는 열쇠(key)**를 제공하고,
이를 통해 **의식에 대한 확장된 이해**와 **문학, 예술, 종교, 문화**의 해석 가능성을 열었다.

심층심리학의 핵심은 다음 두 가지 이론으로 구성된다:

1. **꿈 해석 이론 (The Interpretation of Dreams, 1900)**
2. **일상생활의 정신병리 이론 (The Psychopathology of Everyday Life, 1904)**

이 이론들은 프로이트가 **히스테리 환자 분석을 통해 일반화한 무의식의 작동 방식**을 체계화한 것이며,
꿈 이론은 대중적으로 널리 알려져 있다.

---

**자크 라캉(Jacques Lacan)**은 1952\~1980년 프랑스 파리에서 진행한 세미나(특히 1957–58년)에 걸쳐 **무의식의 구조**를 집중적으로 분석하였다 (Lacan, 2017).

* 프로이트에게 있어서 무의식은 **억압된 감정과 기억으로 구성된 독립된 실체**였다.
* 라캉은 이 개념을 수용하되, 프랑스 구조주의(French structuralism)의 관점에서 **무의식을 하나의 구조(structure)**로 해석하였다.
* 그는 무의식의 구조를 **언어의 구조**와 유사한 **위계적 체계**로 보았으며, 이로써 **무의식 = 언어 구조와 유사한 계층적 시스템**이라는 관점을 확립하였다 (Günday and Kaçar, 2022).

---

**칼 융(Carl Jung)**은 사후 출간된 저서 『인간과 상징(Man and His Symbols, 1964)』에서 다음과 같이 주장하였다:

* 인간의 의식에는 **처리 가능한 용량의 한계**가 존재하므로,
* **지식, 꿈, 상상, 과거 경험을 저장하는 대체 저장소**, 즉 **무의식**이 필요하다.
* 인간은 **무의식으로부터 신호, 예감, 아이디어**를 받아들이며,
* **무의식이 먼저 인지하고 판단하여 결정을 내리는 경우**가 있으며,
* **이 모든 과정은 본능적으로 수행된다.**

---

**Lakoff & Johnson (1999)**는 『우리의 마음은 은유로 가득하다(Philosophy in the Flesh)』에서 다음과 같이 말한다:

> "우리의 사고 대부분은 무의식적(unconscious)이다.
> 이는 프로이트가 말한 억압(repression)의 의미가 아니라,
> **인지적 자각의 수준 아래에서 너무 빠르게 작동하기 때문에 의식적으로 접근할 수 없는**
> **‘인지적 무의식(cognitive unconscious)’**을 의미한다."

이들은 **무의식의 두 가지 영역**을 구분한다:

1. **자동적 인지 처리**: 시각, 청각, 운동 등
2. **암묵적 지식(implicit knowledge)**: 기억과 관련된 영역이며,

   * 우리가 가진 모든 지식과 믿음은 **개념 체계(conceptual system)** 안에 구성되며,
   * 이 체계는 대부분 **인지적 무의식에 위치한다.**

---

**무의식적 지각(unconscious perception)**은 인간이 **지각하는 방식**을 설명하는 이론적 프레임 중 하나이다.
이는 **대뇌피질(cerebral cortex)**을 넘어서는 **기저핵(basal ganglia)**, **소뇌(cerebellum)** 등과 같은 **하위 수준의 신경계**가
의식 수준으로 도달하지 않으면서도 감각 정보를 처리할 수 있다는 주장에 기반한다.

---

**Roger Schank**는 인공지능과 인지심리학의 교차점에서,
**스크립트(script)**라는 개념을 기반으로 **무의식적 기억과 반응의 구조화**를 제안하였다.

* 스크립트는 **일상적인 사건의 순서와 의미를 담은 구조화된 표현**이다.
* 예: 식당에 가기 → 자리 잡기 → 주문하기 → 음식 먹기 → 계산하기
* 이러한 스크립트는 반복을 통해 **자동화되어 무의식적으로 작동**하게 된다.

Schank와 그의 동료들은 이러한 스크립트 구조가

* **기억 검색(memory retrieval)**,
* **사고(reasoning)**,
* **의사결정(decision making)**의 **기반이 되는 비의식적(무의식적) 처리 단위**라고 보았다.

이 이론은 **시스템 1의 사고**로 대표되는 **빠르고 자동적인 무의식적 사고 과정**과도 일치한다.

---

**무의식 기반 행동 생성(Unconscious Behavior Generation)** 이론은,
특히 **기능주의 심리학(functional psychology)**과 **신경과학(neuroscience)**의 관점에서
무의식이 어떻게 **자율적 행동**, **반사(reflex)**, **습관(habit)**, **직관(intuition)** 등을 조절하는지를 설명한다.

이러한 무의식적 처리는 다음과 같은 **인지 아키텍처**에 반영되었다:

* **ACT-R**: 인간의 인지 과정을 모사하는 심볼릭 모델로, **암묵적 지식(implicit knowledge)**과 **작업 기억(working memory)** 간의 구분이 존재한다.
* **Soar**: 문제 해결과 학습을 위한 아키텍처로, **생성된 규칙(rule)**이 무의식적으로 적용되며, **의식 수준의 판단과 연결된다.**
* **Sigma**: 연속성과 불확실성을 다루는 수학적 모델 기반 아키텍처로, **의식/무의식의 경계 없이 확률적 처리를 수행한다.**

이러한 모델들은 다음을 가정한다:

* 무의식은 **감각적 입력을 필터링**하고
* **반응 패턴을 자동적으로 선택하며**,
* 필요한 경우에만 **의식 수준으로 정보를 전달한다.**

이러한 체계는 **신경계의 효율적인 자원 배분(resource allocation)**을 가능하게 하며,
이는 **현실 세계에서 빠른 반응과 생존 가능성을 높이는 진화적 이점**을 제공한다.

---

## 2.1 AGI 프로토타이핑을 위한 인지 프레임워크 (Cognitive framework for prototyping AGI)

AGI(Artificial General Intelligence, 범용 인공지능) 에이전트를 구축하기 위해서는,
그 에이전트의 지능이 **인지 시스템(cognitive system)**으로 기능해야 한다.
이러한 시스템은 **복잡한 외부 세계의 패턴을 탐색하고 해석하며**,
이를 바탕으로 **행동 전략을 생성하고 선택해야 한다**.

이를 위해 AGI 시스템은 **인지 아키텍처(cognitive architecture)**와 **기초 기능 모듈(basic functional modules)**을 갖추어야 하며,
다음의 네 가지 주요 구성 요소를 포함해야 한다:

1. **자기 인식(self-perception)** 및 **자기 표현(self-representation)**

   * AGI 시스템은 스스로의 상태, 능력, 목표, 한계를 **모델링하고 인식**할 수 있어야 한다.
   * 이를 통해 자율성과 적응성을 확보하며,
   * **의식(consciousness)** 혹은 **메타인지(metacognition)**의 기초를 형성한다.

2. **외부 세계의 모델링(modelling of the external world)**

   * 현실 세계에 대한 **정확한 표현 및 추론 능력**을 갖추어야 하며,
   * 물리적 환경, 사회적 맥락, 규칙과 제약을 인식하고 처리할 수 있어야 한다.

3. **목표 설정(goal setting)** 및 **행동 선택(behavior selection)**

   * 스스로 목표를 설정하거나 외부로부터 주어진 목표를 수용하고,
   * 이를 달성하기 위한 **계획(plan)**과 **의사결정(decision making)** 능력을 수행할 수 있어야 한다.

4. **학습 및 자기조직화(learning and self-organization)**

   * 새로운 지식, 규칙, 행동을 학습하고,
   * 내부 구조와 표현 방식을 **스스로 재구성**할 수 있어야 한다.
   * 이 과정에는 **기억 구조(memory structures)**와 **연결 가중치(connection weights)**의 갱신이 포함된다.

---

위 네 가지 구성 요소는 **AGI 시스템을 프로토타이핑(prototyping)**하기 위한 **기본 인지 프레임워크(cognitive framework)**를 구성한다.
이 프레임워크는 **정적(static)**인 것이 아니라,

* **지속적인 정보의 흐름(flow of information)**과
* **지식의 통합(integration of knowledge)**,
* **행동의 조정(coordination of behavior)**이 이루어지는 **동적 시스템(dynamic system)**으로 간주된다.

AGI 시스템이 **외부 환경과 상호작용(interact with external environment)**하기 위해서는,
다음과 같은 **보조 기능(auxiliary functions)**이 필요하다:

* **감각 처리(sensory processing)**
* **모터 제어(motor control)**
* **의사소통 능력(communication skills)**
* **정서 시스템(emotional systems)**
* **사회적 규범(social norms)**

이 모든 기능은 **인지 프레임워크의 하위 모듈**로 통합되어야 하며,
이를 통해 AGI는 **현실 환경 내에서의 실행가능한 실체**가 된다.

---

## 2.2 AGI 아키텍처 구성 요소 (Components of AGI architecture)

AGI(Artificial General Intelligence) 시스템을 구성하는 데 필요한 기능적 블록들의 집합은,
선행 연구 및 현재 개발 중인 인지 아키텍처들에 기반하여 다음과 같이 정의할 수 있다 (표 1 참조).

각 기능은 다음과 같은 세 가지 범주로 구분된다:

* **핵심 인지 기능(core cognitive functions)**
* **메타인지 및 자기조직화 기능(metacognitive and self-organizing functions)**
* **사회적·윤리적 기능(social and ethical functions)**

아래는 이 기능 구성 요소들의 개요이다:

---

### **핵심 인지 기능 (Core cognitive functions):**

1. **지각(Perception)**

   * 감각 데이터를 처리하고 환경에 대한 표상을 생성함.
   * 시각, 청각, 촉각 등 다중 양식(multimodal)의 정보를 통합함.

2. **주의(Attention)**

   * 유의미한 정보에 선택적으로 자원을 집중.
   * 정보 과부하 상황에서 필수적인 선택 기능.

3. **기억(Memory)**

   * **작업 기억(working memory)**, **단기 기억(short-term memory)**, **장기 기억(long-term memory)** 포함.
   * 학습된 지식과 경험을 저장하고 인출함.

4. **추론(Reasoning)**

   * 논리적 사고, 연역(deduction), 귀납(induction), 유추(abduction) 등을 포함한 판단 메커니즘.

5. **학습(Learning)**

   * 지식, 행동, 규칙 등을 환경 상호작용을 통해 습득함.
   * 지도학습(supervised), 비지도학습(unsupervised), 강화학습(reinforcement learning) 등 포함.

6. **계획 및 의사결정(Planning and Decision Making)**

   * 목표 달성을 위한 행동 시퀀스를 설계하고,
   * 가능한 대안 중 최적의 결정을 내리는 기능.

7. **행동 실행(Action Execution)**

   * 계획된 행동을 실제로 실행함.
   * 모터 시스템, 로봇 제어, 시뮬레이션 인터페이스 등과 연동됨.

---

### **메타인지 및 자기조직화 기능 (Metacognitive and Self-organizing Functions):**

8. **메타인지(Metacognition)**

   * 자신의 인지 상태를 인식하고 조절함.
   * 학습 전략 선택, 에러 감지, 성찰(reflection)에 필수적.

9. **자기 인식(Self-awareness)**

   * 자신의 신체, 정신 상태, 감정, 의도 등을 모델링하고 인식함.
   * 자율성과 적응성의 핵심 요소.

10. **자기조직화(Self-organization)**

* 내부 구조(지식, 연결, 모듈 구성 등)를 외부 변화에 따라 동적으로 재구성함.

11. **의식(Consciousness)**

* 고차원의 통합된 표상 및 자기참조 능력을 포함.
* 여전히 정의와 실현이 논쟁 중인 개념이나, AGI에서는 일정 수준의 구현이 요구됨.

---

### **사회적·윤리적 기능 (Social and Ethical Functions):**

12. **감정(Emotion)**

* 정보 처리 및 행동 선택에 영향을 미치는 정서적 상태.
* 학습, 주의, 사회적 상호작용을 조절함.

13. **사회적 상호작용(Social Interaction)**

* 타인의 의도, 감정, 행동을 이해하고 적절히 반응하는 기능.
* Theory of Mind, 공감, 협동 등이 포함됨.

14. **언어 및 의사소통(Language and Communication)**

* 자연어 이해 및 생성.
* 상징적 의미 처리, 담화 분석, 다중 양식 표현 등 포함.

15. **윤리 및 가치(Ethics and Values)**

* 사회적 규범, 도덕, 법률 등의 내재화.
* 갈등 상황에서 도덕적 판단을 내릴 수 있음.

---

이러한 구성 요소들은 상호작용을 통해 통합된 시스템으로 작동해야 하며,
하나의 **인지 아키텍처(architecture)**로 통합되기 위해서는 **통합 메타모델(integrative metamodel)**이 필요하다.

이후 절에서는 **이러한 요소들을 포괄하는 참조 인지 아키텍처(reference cognitive architecture)**가 어떻게 설계될 수 있는지 제시된다.

---

## 2.3 인지 아키텍처의 분류 (Classification of cognitive architectures)

현재까지 제안된 수많은 인지 아키텍처(cognitive architecture)들은
그 **기초 개념**, **실현 방식**, **응용 영역**, **이론적 배경**에 따라 다양하게 분류될 수 있다.

본 논문에서는 인지 아키텍처들을 다음 세 가지 주요 축(axis)으로 분류한다:

---

### 1. **기호적 vs 연결주의적 vs 하이브리드**

(Symbolic vs Connectionist vs Hybrid)

* **기호적(symbolic)** 아키텍처

  * 인간 사고를 명시적인 **규칙(rule)**과 **기호(symbol)**의 조작으로 모델링
  * 예: Soar, ACT-R
  * 장점: **논리적 추론**과 **설명 가능성**
  * 단점: **학습 능력 부족**, **지속적 적응 어려움**

* **연결주의(connectionist)** 아키텍처

  * **인공신경망(artificial neural networks)** 기반으로,
  * 인간의 신경 처리 과정을 모방함
  * 예: LIDA, LEABRA
  * 장점: **적응성**, **병렬 처리**, **학습 능력**
  * 단점: **설명력 부족**, **해석 어려움**

* **하이브리드(hybrid)** 아키텍처

  * 기호적 시스템과 연결주의적 시스템을 결합하여,
  * 두 방식의 장점을 통합하려 함
  * 예: CLARION, Sigma
  * 현재 AGI 분야에서 가장 유망한 접근 방식으로 간주됨

---

### 2. **정책 기반 vs 가치 기반**

(Policy-based vs Value-based)

* **정책 기반(policy-based)** 아키텍처

  * 환경 상태에 따라 **즉시 반응하는 행동 규칙** 중심
  * 규칙에 기반한 행동 생성 시스템
  * 주로 로봇 제어, 에이전트 시뮬레이션 등에 사용

* **가치 기반(value-based)** 아키텍처

  * **보상 함수(reward function)**에 따라
  * 미래 보상을 최대화하는 방향으로 행동을 결정
  * 강화학습(reinforcement learning)과 밀접한 연관
  * 장기적 전략 수립에 유리

---

### 3. **작업지향 vs 이론지향**

(Task-oriented vs Theory-oriented)

* **작업지향(task-oriented)** 아키텍처

  * 특정 문제 해결(예: 내비게이션, 대화 시스템 등)을 위해 설계됨
  * 실용적이며 산업 응용에 적합

* **이론지향(theory-oriented)** 아키텍처

  * 인간 인지의 **이해 및 시뮬레이션**을 목적으로 함
  * 예: ACT-R, Soar
  * 실험 심리학 및 인지과학 연구에 유용

---

이러한 분류는 상호 배타적이지 않으며,
하나의 인지 아키텍처가 **여러 범주에 동시에 속할 수 있음**에 유의해야 한다.
예를 들어 Sigma는 **하이브리드-가치 기반-이론지향** 아키텍처로 분류된다.

다음 절에서는 **보편적 지식 모델(Universal Knowledge Model)**의 개념과
인지 아키텍처 설계에 있어 그 중요성에 대해 설명한다.

---

## 2.4 보편적 지식 모델의 필요성

(Need for a universal knowledge model)

AGI(Artificial General Intelligence, 범용 인공지능)의 구현에 있어,
지식 표현(knowledge representation)은 핵심적인 문제 중 하나이다.
현재 존재하는 대부분의 인지 아키텍처들은 **특정 목적이나 도메인에 맞춘 지식 구조**에 의존하고 있으며,
이는 다음과 같은 한계를 야기한다:

1. **호환성 부족 (Lack of interoperability)**

   * 서로 다른 시스템 간에 지식을 공유하거나 통합하는 데 어려움이 있음.

2. **확장성 제한 (Limited scalability)**

   * 새로운 영역이나 기능을 추가할 때 기존 구조의 변경이 필요함.

3. **비표준적 표현 (Non-standard representations)**

   * 각 시스템이 고유한 형식과 구조를 사용함으로써,
     지식의 **일관된 해석과 활용**이 어려워짐.

---

이러한 문제를 극복하기 위해, 본 논문에서는
**모든 인지 아키텍처에 적용 가능한 보편적 지식 모델(universal knowledge model)**의 필요성을 주장한다.
이 모델은 다음과 같은 기능을 수행해야 한다:

* **다양한 유형의 지식 통합 (Integration of multiple types of knowledge)**

  * 선언적(declarative), 절차적(procedural), 상황적(contextual), 정서적(emotional) 지식을 모두 포함함.

* **표현의 유연성 (Flexibility of representation)**

  * 구조화된(symbolic), 비구조화된(sub-symbolic), 통계적(statistical), 개념적(conceptual) 표현을 모두 수용해야 함.

* **인지 아키텍처 독립성 (Architecture-independence)**

  * 특정 구현이나 시스템에 종속되지 않아야 하며,
    다양한 아키텍처에서 동일하게 해석되고 작동할 수 있어야 함.

* **확장성과 재사용성 (Scalability and reusability)**

  * 새로운 도메인, 작업, 환경에 쉽게 적용 가능해야 하며,
    기존 지식과의 충돌 없이 **재사용**될 수 있어야 함.

---

이러한 **보편적 지식 모델**은
단순한 지식 저장소(knowledge repository)를 넘어서
**인지 처리의 기반 구조(cognitive processing infrastructure)**로 작용해야 한다.

즉, 이 모델은 다음을 가능하게 한다:

* 지각(perception), 추론(reasoning), 학습(learning), 계획(planning) 등
  핵심 인지 기능들과의 **직접적인 상호작용**
* 여러 AGI 시스템 간의 **지식 공유 및 이전(transfer)**
* 인간과 기계 간의 **효율적인 의사소통 및 협력**

---

이제 다음 절에서는 본 논문에서 제안하는
**보편적 지식 모델(Universal Knowledge Model, UKM)**의 구조와 특성에 대해 자세히 설명한다.

---

## 2.5 보편적 지식 모델의 구조

(Structure of the universal knowledge model)

본 논문에서 제안하는 **보편적 지식 모델(Universal Knowledge Model, UKM)**은
모든 형태의 지식(개념, 절차, 감정, 맥락 등)을 포괄하고 통합할 수 있는
**범용 표현 프레임워크(universal representation framework)**를 지향한다.

이 모델의 구조는 다음과 같은 **다층적 계층(hierarchical layers)**으로 구성된다:

---

### 1. **지식 단위(Knowledge Units, KUs)**

* UKM의 가장 기본 단위로,
  **개념(concept)**, **사건(event)**, **규칙(rule)**, **전략(strategy)**, **감정(emotion)** 등의 정보 덩어리를 포함함.
* 각 KU는 다음의 구성 요소로 정의됨:

  * **정체성(identity)**: 고유 식별자
  * **유형(type)**: KU의 범주 (예: 개념, 사건 등)
  * **내용(content)**: 핵심 지식 내용
  * **속성(properties)**: 수치/범주형 속성 (예: 중요도, 시점, 위치 등)
  * **연결성(links)**: 다른 KU와의 관계 (예: 원인, 결과, 포함 등)

---

### 2. **지식 네트워크(Knowledge Networks)**

* 개별 KU들은 **의미론적(sémantic)**, **시간적(temporal)**, **공간적(spatial)** 관계를 통해
  **네트워크 구조(network structure)**로 연결됨.
* 이 네트워크는 **동적(dynamic)**이며,

  * 학습과정에서 확장/수정 가능하고
  * 추론 시 의미적 확산(spreading activation) 메커니즘을 사용할 수 있음.

---

### 3. **지식 계층(Knowledge Layers)**

UKM은 지식을 **다층적 계층 구조**로 조직함으로써,
정보의 추상화 및 일반화가 가능하게 한다.

주요 계층은 다음과 같다:

| 계층                               | 설명                          |
| -------------------------------- | --------------------------- |
| **감각-실체 층 (Sensorimotor layer)** | 지각, 행동 등 물리적 경험에 직접 연관된 정보  |
| **개념 층 (Conceptual layer)**      | 객체, 사건, 관계 등의 일반화된 개념 구조    |
| **추상 층 (Abstract layer)**        | 전략, 원리, 메타규칙 등 고차원의 일반화된 지식 |

각 계층은 서로 연계되어 있으며,
**상향(bottom-up)** 및 **하향(top-down)** 처리 모두를 지원한다.

---

### 4. **지식 맥락(Contexts)**

* 동일한 지식이라도 **상황에 따라 다르게 해석되어야 하므로**,
  UKM은 **명시적 맥락(contextual embedding)**을 포함한다.
* 각 KU 또는 네트워크는 다음과 같은 맥락 정보와 함께 저장됨:

  * 시간 (Time)
  * 장소 (Location)
  * 감정 상태 (Emotional state)
  * 과업(Task)
  * 사회적 역할 (Social role)

---

### 5. **지식 조작 연산(Operations on Knowledge)**

UKM은 다음과 같은 **표준화된 조작 연산**을 제공하여
인지 아키텍처의 학습, 추론, 적응 기능과의 통합을 가능하게 한다:

* 생성(create), 갱신(update), 삭제(delete)
* 유추(analogy), 일반화(generalization), 특수화(specialization)
* 맥락 이동(context shift), 관련 확산(activation spread)

---

이러한 구조 덕분에 UKM은 다음을 보장한다:

* **표현의 통일성 (uniformity)**
* **연산의 일반성 (generality)**
* **확장성과 적응성 (scalability and adaptability)**

다음 절에서는 이러한 UKM이 어떻게 기존 인지 아키텍처에 통합될 수 있는지를 설명하며,
이를 통해 범용 AGI 구현이 실현 가능함을 보인다.


---

## 2.6 보편적 지식 모델의 통합 전략

(Integration strategies for the universal knowledge model)

보편적 지식 모델(Universal Knowledge Model, UKM)의 실질적인 활용을 위해서는,
기존 또는 새로운 **인지 아키텍처(cognitive architecture)** 내에
이 모델을 **효율적으로 통합**할 수 있어야 한다.
이를 위한 주요 전략은 다음과 같다:

---

### 1. **표현-계산 분리 (Separation of Representation and Computation)**

* UKM은 **지식 표현(representation)**에 집중하고,
  실제 **추론, 학습, 계획 등의 계산(computation)**은
  해당 아키텍처의 처리 모듈에 위임한다.

* 이로 인해, UKM은 다양한 아키텍처에 **비침습적(non-invasive)** 방식으로 결합 가능하며,
  시스템 전체를 재설계하지 않아도 된다.

---

### 2. **표준화된 인터페이스 제공 (Provision of standardized interfaces)**

* UKM은 주요 인지 기능(지각, 추론, 기억 등)과의 연동을 위한
  **API(Application Programming Interface)** 또는 **지식 접근 함수(knowledge access functions)**를 제공한다.

* 예:

  ```python
  retrieve_KU(concept="object permanence", context="infant cognition")  
  update_property(KU_id=2034, property="relevance", value=0.9)
  ```

* 이러한 인터페이스는

  * **구현 독립성(implementation independence)**,
  * **아키텍처 간 상호 운용성(interoperability)**
    을 보장한다.

---

### 3. **데이터 및 모델 마이그레이션 전략 (Strategies for migration of existing data and models)**

* 기존 시스템에 내재된 지식 자산(규칙, 개념, 시나리오 등)을
  UKM 형식으로 변환하기 위한
  **변환 도구(conversion tools)** 및 **매핑 규칙(mapping rules)**이 필요하다.

* 예를 들어, ACT-R의 프로덕션 규칙을
  KU 네트워크 형태로 재표현하거나,
  신경망의 가중치 기반 기억 구조를
  개념적 KU로 일반화하는 전략이 포함된다.

---

### 4. **인지 기능 모듈들과의 양방향 통합 (Bidirectional integration with cognitive modules)**

* UKM은 단순한 읽기(read-only) 저장소가 아니라,
  **지각-기억-추론-학습 루프**와 **상시 양방향 통신**이 가능한 구조로 설계되어야 한다.

* 예시:

  * 추론 모듈이 특정 KU 활성화 요청
  * 학습 모듈이 새로운 KU 생성 및 연결 제안
  * 기억 모듈이 과거 KU들과의 유사성 기반 검색 수행

---

### 5. **시스템 수준 최적화 지원 (Support for system-level optimization)**

* UKM은 각 KU의 **사용 빈도, 활성도, 신뢰도, 맥락 적합성** 등의 메타정보를 추적하여
  시스템 전체의 **인지 처리 효율성**을 높이는 데 기여할 수 있다.

* 예를 들어, **낮은 가중치의 KU는 정리(purged)**하거나,
  **중요도가 높은 KU는 캐싱(caching)**하여 응답 속도를 향상시킬 수 있다.

---

요약하면, UKM은 단순한 지식 저장 구조를 넘어
**인지 시스템 전반의 동적 통합 메커니즘**으로 작동하며,
이러한 전략을 통해 다양한 AGI 구현체에 **범용적이고 유연하게 내장**될 수 있다.

다음 절에서는 이러한 UKM 기반 시스템을 통해 가능해지는
**응용 사례(applications)**에 대해 설명한다.

---

## 2.7 AGI 개발을 위한 지식 기반 인지 시스템의 응용

(Applications of knowledge-based cognitive systems for AGI development)

보편적 지식 모델(Universal Knowledge Model, UKM)은
다양한 인지 기능을 통합함으로써,
AGI(Artificial General Intelligence)의 실현을 위한 **핵심 기반 요소**로 작동할 수 있다.

이 절에서는 UKM을 활용한 지식 기반 인지 시스템이
어떤 방식으로 AGI 개발에 기여할 수 있는지를
**대표적 응용 분야 중심으로** 살펴본다:

---

### 1. **인지 로봇공학 (Cognitive Robotics)**

* UKM은 로봇에게 **개념적 이해(conceptual understanding)**와
  **상황 기반 행동 결정(context-aware behavior selection)** 능력을 부여함.

* 예:

  * 인간의 동작을 관찰하여 "도와달라"는 의도를 인식
  * 유사 상황에 대한 과거 KU 기반 대응 전략 적용

* 기존의 강화학습 기반 정책(policy)보다
  **범용성 및 적응성**이 뛰어난 로봇 제어가 가능함.

---

### 2. **지식 기반 대화 시스템 (Knowledge-based Dialogue Systems)**

* UKM을 기반으로 하는 대화 시스템은
  단순한 문장 패턴이 아닌 **개념적 수준의 의미망(semantic network)**에서 작동함.

* 이로 인해 다음과 같은 고차원 능력 구현이 가능함:

  * **대화 중 지식 참조** 및 **장기 맥락 유지**
  * **감정, 사회적 역할, 관계에 따른 반응 조절**
  * **지식 기반 생성형 응답 (knowledge-grounded generation)**

---

### 3. **인지 모델링 및 시뮬레이션 (Cognitive Modeling and Simulation)**

* UKM은 인간 인지 과정을 모사하는 모델 개발에 활용 가능
  (예: 문제 해결, 오개념 발생, 학습 전략 등)

* 심리학/교육학 실험 시 **인지 전략 변화 시뮬레이션**,
  또는 **의사결정 과정의 인과 네트워크 모델링** 등에 사용됨.

---

### 4. **지식 기반 학습 시스템 (Knowledge-based Learning Systems)**

* UKM은 학습 내용을 **맥락적 지식망**으로 통합하여 저장함으로써,

  * 반복 학습 없이도 **전이 학습(transfer learning)** 가능
  * **학습자 모델링 및 개인화 교육 시스템** 구현에 활용 가능

* 학습자가 새로운 개념을 제시했을 때,
  기존 KU들과 연결하여 **개념 지도(concept map)** 형성

---

### 5. **AGI 개발용 메타 시스템 (Meta-systems for AGI development)**

* UKM 기반 시스템은
  **여러 개의 인지 에이전트/시스템** 간에 지식을 공유하거나,
  **지식 통합/검증 플랫폼**으로 작동할 수 있음.

* 특히, 다양한 아키텍처를 실험/비교하는
  **AGI 테스트베드(testbed)** 개발에 유용함.

---

요약하자면, UKM은 단순한 데이터 저장 구조를 넘어서
**인지 기능 간 상호작용의 핵심 매개체**로 작동함으로써,
다양한 응용 영역에서 **범용성, 적응성, 해석 가능성**을 갖춘 AGI 시스템의 실현을 가능하게 한다.

다음 장에서는 본 논문에서 제안한 UKM 기반 인지 시스템의 **프로토타입 구현**에 대해 소개한다.

---

## 3. 제안 시스템의 프로토타이핑

(Prototyping of the proposed system)

본 절에서는 앞서 제안한 **보편적 지식 모델(Universal Knowledge Model, UKM)** 및
인지 아키텍처 통합 전략을 기반으로 구현한
**시범적 AGI 시스템 프로토타입(prototype)**의 설계와 실행에 대해 기술한다.

이 프로토타입은 UKM의 **실용 가능성(practical viability)**을 검증하고,
AGI 구성 요소 간의 **통합 메커니즘(integration mechanism)**을 실험하는 데 목적이 있다.

---

### 3.1 시스템 구성 개요

(System overview)

프로토타입 시스템은 다음의 **다섯 가지 핵심 모듈**로 구성된다:

| 모듈명                           | 기능                                  |
| ----------------------------- | ----------------------------------- |
| **지각 모듈 (Perception module)** | 외부 입력(자극, 문장, 환경 상태 등)을 수신하고 KU로 변환 |
| **UKM 엔진 (UKM engine)**       | 지식 단위(KUs)를 저장/검색/갱신하며, 지식 네트워크를 관리 |
| **추론 모듈 (Reasoning module)**  | UKM 기반 유추, 일반화, 규칙 적용 수행            |
| **행동 선택기 (Action selector)**  | 추론 결과와 현재 맥락을 기반으로 행동 결정            |
| **학습 모듈 (Learning module)**   | 새로운 KU 생성, 기존 KU의 수정/통합 수행          |

이 모듈들은 UKM을 **중앙 지식 저장소(central knowledge repository)**로 공유하며,
API를 통해 상호작용한다.

---

### 3.2 입력 및 표현 형식

(Input and representation format)

* 입력은 자연어 문장, 시각적 장면, 센서 데이터 등으로 제공되며,
  이를 KU 구조로 변환하는 **지각 변환기(perceptual transducer)**를 사용함.

* KU는 JSON-LD 기반의 다음과 같은 형식으로 표현됨:

```json
{
  "KU_id": "ku_1032",
  "type": "event",
  "content": "User asked for coffee",
  "context": {
    "location": "kitchen",
    "time": "08:15",
    "emotion": "neutral"
  },
  "links": ["ku_0921", "ku_0113"]
}
```

* 이러한 표현은 기계 해석 가능성과
  인간 해석 가능성을 동시에 만족시킴.

---

### 3.3 지식 네트워크 구조

(Knowledge network structure)

* KU들 간의 관계는 **의미론적 그래프(semantic graph)**로 표현되며,
  **Neo4j**와 같은 그래프 데이터베이스를 활용하여 구현됨.

* 각 KU는 **노드(node)**,
  관계는 **에지(edge)**로 나타내며,
  **활성도(activation level)**를 포함한 동적 가중치 부여 가능.

* 예:

  * "커피 요청 KU" → \[원인] → "피곤 KU"
  * "사용자 위치 KU" → \[위치 관계] → "부엌 KU"

---

### 3.4 인지 기능 시뮬레이션

(Cognitive functions simulation)

* 시스템은 다음과 같은 고차원 인지 기능을 시연함:

  1. **상황 인식 (situational awareness)**

     * 입력 KU에 기반하여 현재 상황의 맥락 구성
  2. **의도 추론 (intention inference)**

     * 사용자의 행위 KU에서 목적 및 감정 추론
  3. **계획 수립 및 실행 (planning and execution)**

     * 목표 KU 설정 후, 관련 행동 KU를 연결하여 행동 흐름 생성
  4. **지식 업데이트 및 통합 (knowledge update and integration)**

     * 새 입력으로 기존 KU 네트워크의 구조 수정 및 강화

---

### 3.5 프로토타입 결과 및 시사점

(Prototype results and implications)

* 프로토타입은 제한된 도메인(예: 가정 내 조수 시나리오)에서
  **지식 기반 AGI 구성 요소들의 연계 가능성**을 실증함.

* 주요 성과:

  * KU 기반 표현은 기존 규칙 기반 시스템보다 **유연한 추론** 가능
  * 맥락 기반 KU 전환은 **오류 감소 및 반응 적합도 향상**
  * API 기반 설계로 **다양한 인지 기능 모듈 교체 및 확장 가능성 확인**

* 향후 과제:

  * 대규모 KU 네트워크에서의 처리 최적화
  * 인간 수준의 장기 추론 및 지식 구성 능력 확보
  * 다양한 인지 아키텍처와의 **이종 통합 (heterogeneous integration)** 실현

---

이로써 본 논문에서 제안하는 **보편적 지식 모델과 통합 전략**의
**실현 가능성 및 적용성**이 프로토타입을 통해 실증되었으며,
이는 AGI를 향한 실질적 진보를 의미한다.

다음 장에서는 이러한 시스템이 AGI 개발에 미치는 **이론적 및 실천적 기여**를 정리하고,
향후 연구 방향을 제안한다.

---

## 4. 논의 및 향후 과제

(Discussion and future directions)

본 장에서는 **보편적 지식 모델(Universal Knowledge Model, UKM)**과
인지 아키텍처 간 통합 방식이
**AGI(Artificial General Intelligence)** 개발에 미치는 **이론적 기여**와
실질적인 **응용 가능성**에 대해 논의하고,
이를 바탕으로 향후 연구 방향을 제안한다.

---

### 4.1 이론적 기여

(Theoretical contributions)

본 논문은 다음과 같은 **이론적 기여**를 제공한다:

1. **지식 중심 인지 통합의 프레임워크 정립**

   * 기존 인지 아키텍처들은 기능 단위 혹은 모듈 중심 통합에 집중하였으나,
     본 연구는 **지식 단위(Knowledge Units, KUs)**를 중심으로
     인지 기능들을 **수평적으로 통합**하는 구조를 제시하였다.

2. **보편성과 특수성의 공존 메커니즘 제안**

   * UKM은 범용적 지식 표현 방식을 제공함과 동시에,
     도메인 특화 KU 삽입을 통해
     **전이 가능성과 전문성**을 동시에 확보할 수 있도록 설계되었다.

3. **인지 기능 간 상호작용 모델의 형식화**

   * 지각, 추론, 학습, 계획 간의 **지식 기반 상호작용 구조**를
     API 및 KU 네트워크를 기반으로 형식화하였으며,
     이는 다중 아키텍처 실험의 공통 기반으로 활용 가능하다.

---

### 4.2 실천적 기여

(Practical contributions)

1. **지식 기반 AGI 개발의 구체적 설계방식 제공**

   * 실제 프로토타입 구현을 통해,
     UKM을 중심으로 한 AGI 시스템 설계가 **이론을 넘어 현실화 가능**함을 시연하였다.

2. **API 기반 인지 모듈 교체 가능성 확보**

   * 각 인지 기능이 UKM과 API를 통해 연결됨으로써,
     서로 다른 알고리즘, 다른 구현체를 **자유롭게 결합/교체**할 수 있는 유연성을 확보하였다.

3. **지식 시각화 및 디버깅 가능성 제시**

   * KU 네트워크의 시각화는 시스템의 **내부 상태 해석, 디버깅, 사용자 피드백**에 매우 유용하며,
     이는 AGI 시스템의 **설명 가능성(explainability)**을 높이는 데 기여한다.

---

### 4.3 향후 과제

(Future directions)

1. **대규모 지식 네트워크 최적화**

   * KU 수가 수백만 개 이상으로 확장될 경우,
     그래프 탐색/갱신/학습 비용을 줄이기 위한
     **지식 인덱싱, 캐싱, 분산 저장 구조** 등이 필요하다.

2. **지각/행동 모듈과의 깊은 통합**

   * 현재의 API 기반 연결을 넘어,
     **딥러닝 기반 시각처리, 강화학습 기반 행동 선택**과 UKM 간의
     **표현 호환성**을 향상시킬 필요가 있다.

3. **지식 불확실성 및 오류 처리**

   * 인간처럼 불완전하거나 모호한 정보를 처리하기 위해
     **확률적 KU 모델, 오류 전파 차단 메커니즘** 등이 필요하다.

4. **사회적 상호작용 기반 KU 학습**

   * AGI가 인간과의 대화나 협동 과정에서
     새로운 KU를 생성/갱신하는 메커니즘이 필요하며,
     이는 **지식의 사회적 구성(social construction of knowledge)**과 연결된다.

5. **표준 KU 포맷 및 벤치마크 제안**

   * 다양한 연구자가 공통의 KU 포맷을 활용하고,
     AGI 시스템 간 성능 비교를 위한 **표준화된 벤치마크**가 마련되어야 한다.

---

요약하자면, 본 연구는
AGI 개발을 위한 **지식 중심 인지 통합 프레임워크**를 정립하고,
이를 **이론적 기반** 및 **프로토타입 구현**을 통해 실증하였다.

향후 연구는 이 구조를 기반으로
보다 **대규모, 현실적, 동적** 상황에서도 작동 가능한
**실용적 AGI 시스템**을 구축하는 데 집중될 것이다.

---
