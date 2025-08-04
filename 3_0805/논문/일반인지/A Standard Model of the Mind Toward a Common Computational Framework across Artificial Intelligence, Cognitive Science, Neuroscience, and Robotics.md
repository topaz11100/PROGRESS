**"A Standard Model of the Mind: Toward a Common Computational Framework across Artificial Intelligence, Cognitive Science, Neuroscience, and Robotics"**
---

### 초록 (Abstract)

표준 모델(standard model)은 특정 과학 분야 내에서 하나의 일관된 영역에 대한 **공동체의 합의(consensus)**를 포착하여, 연구와 응용 양측에 지침을 제공하고 모델을 확장하거나 수정하려는 노력을 집중시키는 **누적적 참조 지점(cumulative reference point)**의 역할을 합니다. 본 논문에서는 인간과 유사한 마음(humanlike minds), 즉 인간 인지(cognition)에서 발견되는 구조와 과정과 본질적으로 유사한 구조를 가진 **계산적 실체(computational entities)**에 대해 이러한 표준 모델을 개발할 것을 제안합니다.

우리의 가설은, **인지 아키텍처(cognitive architectures)**가 표준 모델을 정의하기 위한 적절한 **계산적 추상화(computational abstraction)**을 제공하지만, 표준 모델 자체가 하나의 인지 아키텍처는 아니라는 것입니다. 제안된 표준 모델은 2013년 AAAI 가을 심포지엄(AAAI Fall Symposium on Integrated Cognition)에서의 초기 합의(consensus)를 기반으로 시작되었으며, 여기에서는 ACT-R, Sigma, Soar라는 세 가지 기존 인지 아키텍처를 종합하여 확장됩니다.

이 표준 모델은 구조 및 처리(structure and processing), 기억 및 내용(memory and content), 학습(learning), 지각 및 운동(perception and motor)이라는 핵심 측면들을 포괄하며, 아키텍처 수준에서의 합의 지점과 합의 부족 지점뿐만 아니라 **남아 있는 불완전성의 잠재적 영역(potential areas of incompleteness)**을 강조합니다. 본 연구는 **마음의 표준 모델(standard model of the mind)**의 추가 개발에 전 세계 연구 커뮤니티가 참여하는 데 있어 중요한 출발점이 되기를 희망합니다.

---

**인공지능(artificial intelligence), 인지과학(cognitive science), 신경과학(neuroscience), 로보틱스(robotics)**는 모두 **마음(mind)**에 대한 우리의 이해에 기여하고 있지만, 각 분야는 저마다 다른 관점에서 연구를 이끌어갑니다.

* **인공지능**은 인공적인 마음(artificial minds)을 구축하는 데 초점을 맞추므로, **지능적인 행동(intelligent behavior)**을 보이는 시스템을 어떻게 구축할 수 있는지가 주요 관심사입니다.
* **인지과학**은 자연스러운 마음(natural minds)을 모델링하는 데 관심이 있으며, 따라서 **인간의 사고(human thought)**를 생성하는 **인지적 과정(cognitive processes)**을 이해하는 데 중점을 둡니다.
* **신경과학**은 뇌(brain)의 구조와 기능을 다루므로, 마음이 어떻게 뇌로부터 생겨나는지에 가장 큰 관심을 둡니다.
* **로보틱스**는 인공적인 신체(artificial bodies)를 만들고 제어하는 데 집중하므로, 마음이 어떻게 그러한 신체를 제어하는지에 관심이 있습니다.

이러한 분야 간 연구는 궁극적으로 마음에 대한 단일한 이해(single understanding of mind)로 수렴하게 될까요? 아니면 많은 가능성이 구조화된 공간(large but structured space of possibilities)으로 남을까요? 혹은 서로 다른 접근들이 얽혀 있는 혼란스러운 상태(cacophony of approaches)로 끝날까요?
이는 현재까지 명확한 답이 존재하지 않는 **심오한 과학적 질문(deep scientific question)**입니다.

하지만 적어도 **인지과학(cognitive science)**과 **신경과학(neuroscience)** 사이에서는 단일한 해답(single answer)이 존재해야 합니다. 이 둘은 동일한 마음, 또는 매우 좁은 범주의 마음을 서로 다른 추상 수준(level of abstraction)에서 연구하고 있기 때문입니다.
생물학적(biological), 인지적(cognitive), 심리학적(psychological) 영감을 받은 인공지능 및 로보틱스 연구 역시 이러한 특정 범주에 포함될 수 있습니다. 특히 이 범주가 약간 추상화된 상태에서 정의된다면 더욱 그렇습니다. 동시에, 생물학적 영감을 추구하지 않더라도 **기능적 이유(functional reasons)**로 동일한 인접 영역에 위치하게 되는 연구들 역시 이 범주에 포함될 수 있습니다.

이러한 넓은 범주를 우리는 **인간과 유사한 마음(humanlike minds)**이라 부릅니다. 이 범주는 인간 인지(human cognition)의 핵심이라고 가정되는 **제한된 합리성(bounded rationality)**(Simon 1957; Anderson 1990)에 더 초점을 맞추며, 일반적인 인공지능 및 로보틱스 연구에서 흔히 강조되는 **최적성(optimality)**과는 차별화됩니다.

이 **humanlike minds**라는 범주는 기존의 **자연적 영감에 기반한 마음(naturally inspired minds)**보다 더 넓습니다. 왜냐하면 여기에 자연적 마음뿐 아니라 기능적으로 연관되어 있지만 자연에 기반하지는 않은 일부 인공 마음도 포함되기 때문입니다. 그러나 동시에 **인간 수준의 지능(human-level intelligence)**이라는 더 넓은 범주보다는 좁습니다. 왜냐하면 이 모델은 그러한 수준의 지능을 갖추었더라도 그 방식을 지나치게 비인간적인(inhuman) 방식으로 달성한 경우는 제외하기 때문입니다.

---

이 글의 목적은 국제 연구 커뮤니티가 인간과 유사한 마음(humanlike mind)을 대상으로 하는 **표준 모델(standard model)** 개발 과정에 참여하는 데 있어 출발점을 마련하는 것입니다. 여기서 우리가 염두에 두고 있는 '마음(mind)'은 바로 **인간과 유사한 마음(humanlike mind)**입니다.

'표준 모델(standard model)'이라는 개념은 물리학(physics)에 그 뿌리를 두고 있으며, 물리학 커뮤니티는 지난 반세기 이상 동안 이 모델을 발전시키고 검증해왔습니다. 그 결과, **입자에 관한 대부분의 지식**을 통합한 모델이 형성되었습니다. 이 모델은 **내적으로 일관성(internal consistency)**이 있는 것으로 간주되지만, 여전히 **중대한 공백(major gaps)**을 가지고 있습니다. 이 모델은 해당 분야의 누적적 참조 지점(cumulative reference point)으로 기능하며, **확장(extension)** 또는 **반례 제시(breaking)**를 통한 지속적인 진보를 이끌고 있습니다.

물리학에서와 마찬가지로, **마음의 표준 모델(standard model of the mind)**을 개발하는 일은 관련 학문 분야 전반의 연구를 가속화할 수 있습니다. 이 모델은 **일관된 기준선(coherent baseline)**을 제공함으로써, **공유된 누적적 발전(shared cumulative progress)**을 촉진할 수 있습니다.

통합적 연구자들(integrative researchers)이 전체 마음을 모델링하는 데 관심이 있을 경우, 표준 모델은 **자신의 접근 방식과 모델 간의 차이점**에 연구 초점을 맞추는 데 도움을 줄 수 있으며, 표준 모델을 **어떻게 확장하거나 수정할 것인가**라는 문제에도 집중할 수 있게 합니다. 또한, 이러한 연구자들이 각자 **자신의 접근 방식의 전제조건과 제약사항**을 처음부터 모두 설명해야 하는 수고를 덜 수 있으며, 단지 **표준 모델과 어떻게 다른지만** 명시하면 됩니다.

예를 들어 이 논문 요약에 수록된 **표 1(Table 1)**과 **표 2(Table 2)**는 본문에서 제안한 표준 모델과, 세 가지 상이한 접근 방식이 해당 모델에 대해 어떤 입장을 취하는지를 명시적으로 보여줍니다. 이와 같은 과정에서 **표준 모델은 일종의 중간 언어(interlingua)** 또는 **공유된 온톨로지(shared ontology)**처럼 기능할 수 있으며, 다양한 인지 아키텍처 간의 **공통된 요소**뿐만 아니라 **서로 다른 용어체계**를 공통 기반에 매핑할 수 있는 수단이 될 수 있습니다.

**이론적/시스템적 연구자들(theoretical and systems researchers)**이 마음의 특정 구성 요소 — 예컨대 학습(learning), 기억(memory), 추론(reasoning), 언어(language) —를 모델링하거나 구축할 때, 표준 모델은 이들이 **다른 구성 요소의 측면을 포함하도록 확장**하고자 할 때 유용한 지침이 될 수 있습니다.
**실험적 연구자들(experimental researchers)**이 자연적인 마음과 뇌의 작동 방식을 세부적으로 밝혀내려 할 때, 표준 모델은 **탑다운 방식의 해석 기준(top-down guidance)**을 제공할 수 있으며, **새로운 실험 가설**을 제시하는 데도 도움이 될 수 있습니다.

모든 연구자에게 있어 표준 모델은, **단일 구성 요소(single component)**나 **여러 구성 요소의 조합**을 평가하기 위해 사용되는 데이터를 체계적으로 구성하고 커뮤니티가 함께 활용할 수 있는 기반이 될 수 있습니다. 나아가, **표준화된 테스트 및 테스트베드**로 발전할 가능성도 있습니다. 표준 모델은 **광범위한 지능형 응용 시스템(intelligent applications)** 구축에 있어서 실무자들에게도 유용한 기반을 제공할 수 있습니다.

---

적어도 예측 가능한 미래(foreseeable future) 동안의 의도는, **모든 인간 유사 마음(humanlike minds)**에 관심 있는 연구자들이 따라야 할 **단일한 구현(single implementation)** 또는 **단일한 마음 모델(single model of mind)**을 개발하거나, **모든 세부 사항에 대해 정확하다고 합의된 이론(a theory in which all of the details are agreed to as correct)**을 만드는 것이 아닙니다.

우리가 추구하는 것은, **커뮤니티의 현재 마음에 대한 이해(current understanding of the mind)**를 바탕으로 한 **최선의 합의(best consensus)**를 선언하는 것이며, 앞으로 더 많은 것을 알게 되었을 때 이를 기반으로 **지속적으로 정교화(refinement)**할 수 있는 견고한 기반을 마련하는 것입니다.

지금까지의 통합적 마음 모델(integrative models of mind)에 관한 연구는 대체로 **이론보다는 구현(implementation)**에 초점을 맞추고 있었으며, 이러한 구현들 간에는 **교류(interchange)**나 **종합(synthesis)**이 거의 일어나지 못했습니다. 그러나 **표준 모델의 개발**은, 이러한 작업들을 보다 **추상적인 수준(more abstract level)**에서 함께 수행할 수 있는 기회를 제공합니다. 이 수준에서는 교류와 통합이 더 실현 가능해질 것입니다.

이러한 일이 실제로 이루어지기 위해서는, **각 연구자들**이 자신의 접근 방식을 **표준 모델과 비교해보려는 관심**을 가져야 하고, 또한 그 모델의 발전에 **적극적으로 참여**해야 합니다. 이 과정에서 연구자들이 **표준 모델의 특정 측면에 동의하지 않게 되는 것**은 충분히 예상 가능한 일이며, 이는 오히려 **그 부분을 반증(disprove)**하거나 **개선(improve)**하려는 노력을 촉진시킬 수 있습니다.

또한, 표준 모델은 **중요한 방식으로 불완전한 상태(significantly incomplete)**일 수밖에 없으며, 이는 빠뜨린 요소들이 **중요하지 않아서가 아니라**, 아직 **이에 대한 충분한 합의(consensus)**가 형성되지 않았기 때문입니다. 따라서 **표준 모델에서 특정 내용이 빠졌다는 것**은 그것의 **존재 유무나 중요성에 대한 부정**이 아니라, 오히려 **합의가 필요한 부분이라는 신호**일 수 있습니다.

---

비록 **인간 유사 마음(humanlike minds)**이라는 범주의 경계(boundary)는 현재로서는 명확히 정의되어 있지 않지만, 우리는 이에 대한 **진화하는 대화(evolving dialogue)**가 앞으로도 지속될 것이라 예상합니다. 이 대화는 **표준 모델(standard model)**과 **실질적인 방식으로 충돌하는(come into conflict in substantive ways)** 아이디어 및 데이터로부터 제기되는 일련의 **도전(challenges)**들에 의해 주도될 것입니다.

이러한 도전(challenges) 하나하나에 대해, 우리는 **궁극적인 합의(consensus)**가 다음 중 어느 쪽에 해당하는지를 결정해야 할 것입니다:

1. 표준 모델을 **수정(altered)**하여 충돌을 제거하거나,
2. 표준 모델을 **추상화(abstracted)**하여 기존 접근과 새로운 접근 모두를 포괄할 수 있도록 만들 것인지,
3. 혹은 새롭게 제기된 아이디어나 데이터가 **인간 유사(humanlike)**하지 않다고 간주되어, 우리가 관심을 가지는 범주 밖에 해당된다고 판단할 것인지.

이러한 결정들은 결코 쉽지 않을 것이며, 전체적인 진행 과정도 순탄하지만은 않을 것입니다. 그러나 **이 과정을 통해 얻을 수 있는 잠재적 보상(potential rewards)**은 분명 실질적입니다.

---

이 글은 2013년 개최된 **AAAI 가을 심포지엄(AAAI Fall Symposium)** 중 **통합 인지(Integrated Cognition)**를 주제로 한 행사에서 시작되었습니다. 이 심포지엄은 우리 저자 중 두 명이 주도하였으며, **인간 수준의 통합적 인지(human-level integrated cognition)**에 관심을 가진 다양한 관점과 커뮤니티의 연구자들을 한자리에 모으기 위한 목적이었습니다 (Burns et al. 2014).

전체 조직위원회는 **인지과학(cognitive science)**, **인지적·생물학적 영감을 받은 인공지능(cognitively and biologically inspired artificial intelligence)**, **범용 인공지능(artificial general intelligence)**, 그리고 **로보틱스(robotics)** 분야의 대표들로 구성되어 있었습니다.

심포지엄의 마지막 활동은 **"합의와 미해결 쟁점(Consensus and Outstanding Issues)"**을 주제로 한 패널 토론이었고, 이 자리에서 저자 중 두 명이 발표를 했으며, 세 번째 저자도 토론에 참여하였습니다.
이 중 하나의 발표는 놀라운 발견으로 이어졌습니다. 당시 그 자리에 있던 다양한 분야의 연구자들이 발표 내용에 대해 **현재 해당 분야의 상태를 잘 나타낸 합의(consensus)**라고 동의한 것입니다.

해당 분야의 오랜 역사 속에서는 **상호 경쟁하는 접근들 간의 극심한 의견 차이(stark differences)**가 지속되어 왔기에, 심포지엄을 시작했던 두 저자조차도 이러한 합의가 가능할 것이라고는 현실적으로 예상하지 못했습니다.
그러나 실제로 이러한 합의가 도출되었고, 그것은 참석자들을 깜짝 놀라게 했습니다. 이는 **이미 암묵적인 합의가 형성되기 시작했음을 시사하는 결과**였으며, 어쩌면 이는 이 분야가 **성숙 단계(maturity)**에 접어들고 있다는 신호일 수도 있습니다.
이러한 **암묵적 합의(implicit consensus)**를 **명시적(explicit)**으로 문서화하려는 시도가 **중대한 가치를 지닐 수 있음**이 그 순간 분명해졌습니다.

---

이러한 시도가 바로 이 글의 나머지 부분을 채우는 내용입니다. 다음 절에서는 2013년 심포지엄과 이 논문이 직접적으로 시작되기 이전의 중요한 배경을 다룹니다. 여기에는 **표준 모델(standard model)** 개념의 몇몇 주목할 만한 선행 사례들뿐만 아니라, 본 시도의 핵심에 해당하는 개념인 **인지 아키텍처(cognitive architecture)**—즉, 마음의 고정된 구조(fixed structure of the mind)에 대한 가설(hypothesis)—가 포함됩니다.

그 후, 본 연구가 집중하여 분석한 세 가지 인지 아키텍처인 **ACT-R**, **Soar**, **Sigma**를 소개합니다.
이 섹션 다음에는, 우리가 개발한 **표준 모델(standard model)**의 구체적인 내용을 제시합니다.

마지막으로 정리(section summary)에서는 지금까지의 성과를 요약하면서,

* 제안된 표준 모델에 대한 **간결한 개요(précis)**,
* 그 모델에 대해 세 아키텍처가 각각 어떤 위치에 있는지를 분석한 내용,
* 이 표준 모델이 **앞으로 어떤 방향으로 나아가기를 기대하는지**에 대한 논의를 포함합니다.

---

### 배경 (Background)

이 글에서 제안하는 **마음의 표준 모델(standard model of the mind)**은 비록 2013년 심포지엄에서 본격적으로 시작되었지만, 결코 무(無)에서 갑자기 생겨난 것이 아닙니다. 그리고 그 이전의 흐름에는 무엇보다 **Allen Newell**의 영향이 깊게 자리하고 있습니다.

약 30년 전의 주목할 만한 선행 사례 중 하나는 **모델 인간 처리기(model human processor)**입니다 (Card, Moran, and Newell 1983). 이 모델은 인간의 **지각(perceptual)**, **정신적(mental)**, **운동(motor)** 과정들에서의 **구조적 및 시간적 규칙성(structural and timing regularities)**에 대한 추상 모델을 정의합니다. 이를 통해 **인간 행동의 대략적인 시간 소요**를 예측할 수 있도록 돕지만, **그 하위에 존재하는 계산적 처리 과정(computational processes)**에 대한 구체적인 설명은 포함하지 않습니다.

두 번째 선행 사례는 성격은 다르지만 역시 중요합니다. 바로 Newell의 1990년 저작에서 제시된, **인지에서 스케일(scale)이 어떻게 작용하는지**에 대한 분석입니다. 그는 인간 활동이 **다양한 시간 척도(time scales)**에 따라 **처리 수준(processing levels)**으로 구분될 수 있다고 보았고, 이를 **100마이크로초(μs)**에서 시작하여 **수 개월**에 이르는 **12개의 서로 다른 크기의 시간 단위**로 배열했습니다.

마음을 연구해 온 다양한 학문 분야들이 각기 다른 시간 척도에 집중해 온 경향이 있지만, 이 분석은 **서로 다른 시간 규모에서의 현상과 기제를 통합적으로 이해**할 수 있는 **일관된 틀(coherent framework)**을 제공합니다. 이는 물리학을 포함한 모든 자연과학에서 나타나는 현상과 유사하며, 시간 및 길이 척도에 따라 분리된 현상들이 **통합적인 다중 척도 모델(multiscale models)**을 구성할 수 있다는 점과도 상통합니다.

---

Newell은 이러한 시간 척도들을 네 개의 범주(band)로 분류하였습니다:
**생물학적(biological)**, **인지적(cognitive)**, **합리적(rational)**, **사회적(social)** 범주입니다.

* 가장 낮은 수준인 **생물학적 범주(biological band)**는 **개별 뉴런과 시냅스(neuron and synapse)**의 처리 시간 척도에 해당하며, 이는 인간 뇌의 기능적 기본 단위로서 **신경과학(neuroscience)**의 주요 연구 대상입니다.
* 그 위에 위치한 **인지적(cognitive)** 및 **합리적(rational)** 범주는 약 **100밀리초(ms)**에서 **수 시간**에 이르는 활동을 포함하며, 이는 **인지과학(cognitive science)**과 전통적인 인공지능(AI)의 연구 대상과 일치합니다. 이 범주에는 **반응적 행동(reactive behavior)**, **목표 기반 의사결정(goal-directed decision making)**, **자연어 처리(natural language processing)**, **계획(planning)** 등이 포함됩니다.
* 가장 상위 범주인 **사회적 범주(social band)**는 **마음 이론(Theory of Mind)**, **조직 행동(organizational behavior)**, **도덕적·윤리적 추론(moral and ethical reasoning)** 등의 고차원 능력을 포함합니다 (예: Scheutz \[2017], Bello and Bridewell \[2017] 참고).

이와 같은 계층(hierarchy)은 **신경과학(neuroscience)**, **심리학(psychology)**, **인공지능(artificial intelligence)**, **경제학(economics)**, **사회학(sociology)**, **정치학(political science)** 등 여러 분야에서 나타나는 연구의 다양성을 설명해 줍니다. 그리고 이러한 계층들은, **마음을 이해하는 데 있어 각기 다른 시간 규모에서의 규칙성(regularities)**이 생산적으로 작용할 수 있다는 점을 시사합니다.

---

인간의 경우, **의도적 행위 수준(deliberate act level)**—약 **100밀리초(ms)** 정도의 시간 척도—은 단순 반응(simple reaction)의 시간 규모에 해당합니다. 물론 이 "단순함"이라는 표현은 다소 모호할 수 있는데, 실제로는 **지각(perception)**, **인지(cognition)**, **행동(action)**을 포함한 여러 내부 과정들이 이 단순한 반응 하나에도 관여하기 때문입니다.

좀 더 포괄적으로 보면, 이 **의도적 행위 수준(deliberate act level)**은 **기초적인 연산(elementary operations)**들이 **선택되고 적용되는 지점**에 해당합니다. 이 수준 및 그 이상에서 **전제되는 핵심 가정(fundamental assumption)**은, **물리적 기호 체계(physical symbol system)**와 유사한 계산 능력이 존재한다는 것입니다.

**물리적 기호 체계 가설(physical symbol systems hypothesis)**은 다음과 같이 서술됩니다:

> “물리적 기호 체계는 일반적인 지능적 행위(general intelligent action)를 위한 **필요충분 조건**을 갖춘다.” (Newell and Simon 1976)

하지만 이번 **표준 모델(standard model)**은 기존의 전통에서 다소 벗어나, **의도적 행위 수준(deliberate act level)**에서의 계산이 **순수하게(symbolically)** 또는 **완전히(symbolically perfectly)** 기호적인 것만은 아니라고 가정합니다.

**기호 체계(symbol systems)**는 **계산 보편성(computational universality)**으로부터 논리적으로 충분함(logically sufficient)을 갖추고 있음이 알려져 있지만, 실제로는 **통계적(statistical)**이거나 **공간적(spatial)**인 방식의 추론이 이 수준에서 직접적으로 수행되어야 하는 경우가 많고, 이런 추론은 **기호적 방식보다는 비기호적(nonsymbolic)** 방식으로 구현하는 것이 더 적합하다는 다수의 증거가 존재합니다.

---

**표준 모델(standard model)**에서 **기호(symbol)**의 핵심 특징은, 그것들이 **관계를 정의할 수 있는 기본 요소(primitive elements)**라는 점에 있습니다. 또한 이러한 기호들을 여러 관계에 걸쳐 사용함으로써, **복잡한 기호 구조(complex symbol structures)**를 만들 수 있다는 것입니다. 이 구조에는 **의미망(semantic networks)**, **온톨로지(ontologies)**, **분류체계(taxonomies)** 등 다양한 형태가 포함될 수 있습니다.

이러한 기호의 사용 방식은 **인지 신경과학(cognitive neuroscience)**에서의 **결합 문제(binding problem)**와 유사합니다. 결합 문제란 여러 요소들이 **구조화된 방식으로 연합(association)**될 수 있는 방법을 다루는 것입니다 (Treisman 1996).

그러나 표준 모델은 **기호의 표현 방식(symbol representation)**에 대해서는 중립적인 입장을 취합니다. 예를 들어:

* 기호는 **해석되지 않은 레이블(uninterpreted labels)**일 수도 있습니다. 이는 Lisp, Soar (Laird 2012), ACT-R (Anderson 2007) 등에서 사용되는 방식입니다.
* 혹은 기호는 **분산된 요소들의 벡터 위에 정의된 패턴(patterns over vectors of distributed elements)**일 수도 있습니다. 예: Spaun 모델의 **의미 지시자(semantic pointers)** (Eliasmith et al. 2012), HDM에서의 **홀로그래픽 벡터(holographic vectors)** (Kelly, Kwock, and West 2015)
* 또는 두 방식이 **공존**할 수도 있습니다. 예: Clarion (Sun 2016), Sigma (Rosenbloom, Demski, and Ustun 2016a)

중요한 것은 표현 방식이 아니라, **관계적 구조(relational structures)**를 **표현하고 조작할 수 있는 기능(functionality)**이 확보되어야 한다는 점입니다.

---

**표준 모델(standard model)**에서 **비기호적 정보(nonsymbolic information)**, 즉 **수치적 정보(numeric information)**는 두 가지 역할을 수행합니다.

1. 첫 번째 역할은 **양적으로 표현된 작업(task)** 정보를 명시적으로 나타내는 것입니다.
   예를 들어,

   * **공간 추론(spatial reasoning)**에서는 거리(distance),
   * **시간 추론(temporal reasoning)**에서는 시간(time)과 같은 정보를 나타냅니다.

2. 두 번째 역할은, **기호적 정보(symbolic information)**와 **비기호적 정보(nonsymbolic information)** 모두에 대해 **처리 방식(processing)**을 조절하기 위해, 이러한 정보 표현을 **주석(annotation)** 형태로 **보강하는 것**입니다.
   다시 말해, 이 두 번째 수치 정보는 **메타데이터(metadata)** 형태를 가지며, 이는 "**데이터에 대한 수치적 데이터(numerical data about data)**"라고 할 수 있습니다.

---

그렇다면 **마음(mind)**은 최소한 **의도적 행위 수준(deliberate act level)** 이상에 해당하는 모든 것을 포함한다고 명확히 말할 수 있습니다. 다시 말해, **Newell의 계층(hierarchy)**에서 **상위 세 개의 범주(bands)**—**인지적(cognitive)**, **합리적(rational)**, **사회적(social)**—가 모두 마음의 구성 요소에 포함된다는 뜻입니다.

하지만 많은 **마음에 대한 개념적 정의들(conceptions of the mind)**은 여기서 더 나아가, **생물학적 범주(biological band)**의 일부도 마음에 포함시키고자 합니다.
이 경우 생물학적 범주는 다음과 같이 모델링됩니다:

* **추상적인 신경 모델(abstract neural model)**, 또는
* **그래프 기반 모델(graphical model)**과 같은 근접 구조 (예: Koller and Friedman 2009)

이러한 생물학적 요소가 포함되든 아니든 간에, **의도적 행위 수준(deliberate act level)**에서 **기호 체계(symbol system)**를 정의할 수 있는 **고정된 구조(fixed structure)**를 모델링하는 것은 곧 **인지 아키텍처(cognitive architecture)**를 구성하는 것입니다.

마음(mind)의 모델은 다양한 수준에서 정의될 수 있지만, 본 논문에서는 모델을 **의도적 행위 수준(deliberate act level)**에 위치시킵니다.
왜냐하면 이 수준이야말로 **그 하부에 존재하는 신경 처리(neural processes)**와,
그 위에 형성되는 **(제한된) 합리적 계산(boundedly rational computations)** 간의 **중요한 연결 지점(critical juncture)**을 형성한다고 보기 때문입니다.

우리가 목표로 삼는 **표준 모델(standard model)**은 바로
**인간 유사 마음(humanlike mind)**을 구현하기 위해
**인지 아키텍처(cognitive architecture)**에 반드시 포함되어야 하는 요소들에 대한 **합의(consensus)**로 정의될 수 있습니다.

---

**초기 인지 아키텍처(cognitive architecture)** 연구들과는 크게 결별하여, 본 **표준 모델(standard model)**은 **상징적(symbolic)** 처리뿐만 아니라 **통계적(statistical)** 처리까지 포괄하는 **혼합형(hybrid)** 접근을 채택합니다. 이는 앞서 언급한 바와 같이, 인지 아키텍처 내부에 **통계적 처리(statistical processing)**가 필요하다는 점을 반영한 것입니다. 초기에는 순수하게 상징적인 처리 모델에 의존했던 것과는 분명히 구분됩니다.

이로 인해 표준 모델은 다음과 같은 요소들을 함께 포함하게 됩니다:

* **베이즈 학습(Bayesian learning)**과
* **강화 학습(reinforcement learning)**을 포함하는 **통계적 학습(statistical learning)** 방식들.

또한 이 모델은 다음과 같은 특성을 갖습니다:

* **모듈 내부(module-internal)**와 **모듈 간(inter-module)** 모두에서의 **병렬성(parallelism)**을 인정하면서도,
* 여전히 **직렬적 병목(serial bottleneck)**을 유지합니다.

즉, 이 모델은 **완전한 직렬 처리(strict seriality)**를 요구하지는 않으며, **병렬성과 직렬성의 혼합 구조**를 지닌다고 볼 수 있습니다.

이러한 전환의 배경 및 **표준 모델을 정의하는 다른 가정들**은, 본 논문의 후반부에서 더욱 상세히 설명됩니다.

---

**인지 아키텍처(cognitive architectures)**에 대한 전형적인 연구들은 (Langley, Laird, and Rogers 2009), 단순히 아키텍처 수준(architectural level)에만 국한되지 않으며, 따라서 오히려 **더 포괄적인 인지 시스템(comprehensive cognitive systems)**을 개발하는 방향으로 이해되는 편이 적절합니다. 하지만 그 어떤 연구도 아직까지는 **전체 계층(hierarchy)**을 아우르지는 못했습니다.

많은 경우, 이러한 연구들은 하나 또는 소수의 수준(level)에서 시작하여, 시간이 지남에 따라 확장됩니다. 그 결과, **다년간 혹은 수십 년에 걸친 연구 프로그램(research programme)**으로 발전하게 되며, 점차 더 많은 수준들을 포괄하게 됩니다 (Lakatos 1970 참고).

그러나, 본 표준 모델은 **마음 전체(the entire mind)**에 대한 직접적인 모델을 제공하려는 것이 아닙니다.

다시 물리학의 사례로 돌아가 보자면, 물리학에서의 **표준 모델(standard model)** 역시 **물리 세계 전체(the entire physical world)**를 직접적으로 모델링하지 않습니다. 그보다는, 상대적으로 **낮은 수준(low level)**인 **입자 수준(particles)**에 초점을 맞추고 있으며, 이 모델은:

* **그보다 높은 수준(higher levels)**—예를 들어 전체 우주(universe) 혹은 다중우주(multiverse)에 이르기까지—에 대한 이해의 **기반(foundation)**을 제공하는 동시에,
* **그보다 낮은 수준(lower levels)**에 의해 **엄격하게 제약(constrained)**받고 있습니다.

마찬가지로, **마음의 표준 모델(standard model of the mind)** 또한 특정 **하나의 수준(one level)**에 직접적으로 초점을 맞추고 있으며, 이 수준을 통해:

* **상위 인지 수준(higher levels of the mind)**에 대한 **핵심 기반(critical foundation)**을 제공하고,
* **하위 신경 수준(lower neural levels)**에 의해 **제약을 받는 구조**를 형성합니다.

---

**마음의 상위 수준(higher levels of the mind)**에 관해서는, **표준 모델(standard model)**에 부수적으로 연결된 하나의 가설(ancillary hypothesis)이 있습니다.
바로 이 상위 수준들은 **인지 아키텍처(cognitive architecture)**에 의해 **획득되고 처리되는 지식과 기술(knowledge and skills)**만으로 정의된다는 것입니다.

간단히 말해, 이 가설은 다음과 같습니다:

> **지능적 행동(intelligent behavior)**은 **인지 아키텍처의 구현(implementation)**과,
> 그 위에 얹혀진 **지식(knowledge)** 및 **기술(skills)**의 조합으로부터 발생한다.

이때 상위 수준에서의 처리는, **시간에 따른 이러한 상호작용의 연속(sequence of interactions over time)**으로 구성됩니다.

예를 들어, **자연어 처리(natural language processing)**나 **계획(planning)**과 같은 복잡한 인지 능력(complex cognitive capabilities)조차도, 고유한 상위 수준 모듈로서 존재한다기보다는,
**인지 아키텍처와 그 위에 축적된 지식**에 의해 **구성된 결과물**로 간주됩니다 (예: McShane \[2017] 참고).

특정 메커니즘들은 때때로 여러 수준으로 분해(decompose)될 수 있습니다.
예를 들어 Forbus와 Hinrichs (2017)의 **유추 처리(analogy process)**는 다음과 같은 방식으로 설명될 수 있습니다:

* **SME(Structure-Mapping Engine)** 메커니즘은 적어도 부분적으로는 **의도적 행위 수준(deliberate act level)**에 위치하며,
* 이와 함께 작동하는 탐색 프로세스(search processes)들 — 예를 들어 **MAC/FAC**, **SAGE** — 는
  더 높은 수준에서 동작하면서 **원시 행위(primitive acts)**로 다시 분해될 수 있습니다.

---

**마음의 하위 수준(lower levels of the mind)** — 즉 **생물학적 범주(biological band)** 또는 그에 해당하는 **인공적 등가 구조(artificial equivalent)** — 는 **인지 아키텍처(cognitive architecture)**를 구현(implement)하고, 동시에 그것에 제약(constraint)을 가합니다.

이 계층적 구조(hierarchy)가 보여주듯, **인지 아키텍처라는 개념**과 **표준 모델(standard model)**은 **신경 모델링(neural modeling)**과 **양립 불가능한 것**이 아닙니다. 오히려, 두 접근 간에는 **호환성(compatibility)**뿐만 아니라, **유익한 상호 보완성(useful complementarity)**도 존재합니다.

예를 들어, **분산 표현(distributed representations)**에서의 일반화(generalization)와 같은 **신경 처리(neural processing)**의 특성은,
인지 아키텍처 내에서 **하위기호적 통계 메커니즘(subsymbolic statistical mechanisms)**의 형태로 구현되어 왔습니다.

반대로, **표준 모델**은 **심층 신경망(deep learning)** 등과 같은 메커니즘에 구조적 기반(architectural structure)을 제공함으로써,
단순한 **기억 능력(memory capabilities)**을 넘어서는 기능이 필요할 때 **조직화 및 보완의 틀**이 될 수 있습니다
(예: Vinokurov et al. \[2012]).

또한, 전통적으로 **고정된 인지 아키텍처(fixed cognitive architecture)**라는 개념은,
**정상적인 추론 과정의 시간 척도(time scale of normal reasoning processes)**에 대해 고정되어 있다는 뜻으로 받아들여졌습니다.
즉, 이는 어떤 **기호 체계(symbol system)**가 반드시 **선천적으로 타고나야 한다**는 의미는 아니며,
**발달 과정(development)** 중에 **새롭게 등장하거나 변화할 수도 있음**을 뜻합니다.

---

**인지 아키텍처(cognitive architecture)**라는 개념은, **Newell**이 그보다 훨씬 이전에 제기했던 비판에서 출발합니다.
그는 다음과 같은 문제를 지적했습니다:
**특정 과제에 특화된 모델들(task-specific models)**은 인지과학(cognitive science)에서 **파편화된 접근(fragmented approach)**을 유발하며, 그 결과로 **누적적인 진보(cumulative progress)**가 어렵다는 점입니다 (Newell 1973).

이러한 문제에 대한 해결책으로, 그는 다음과 같은 개념을 제시했습니다:

> **통합된 인간 인지 모델(an integrated model of human cognition)**을 구축하고, 그 위에
> **공통된 메커니즘과 표현 방식(common set of mechanisms and representations)**을 기반으로
> **특정 과제에 대한 모델들**을 개발하자는 제안이었습니다.
> 궁극적인 목표는 **인지의 통합 이론(Unified Theories of Cognition)**을 달성하는 것이었습니다 (Newell 1990).

이 개념은 **컴퓨터 아키텍처(computer architecture)**와도 유사합니다.
즉, 인지 아키텍처란, **데이터(data)**에 대해 **프로그램(program)**을 실행할 수 있는 **범용 계산 장치(general purpose computational device)**를 정의하는 것입니다.

하지만 여기에는 두 가지 주요 차이점이 있습니다:

1. **인지 아키텍처**에서 지원하는 **프로그램(programs)**과 **데이터(data)**는
   **인간과 유사한 지능적 행동(humanlike intelligent behavior)**을 생성하는 데 적합한 것으로 **제한**됩니다.

2. 이들 **프로그램과 데이터**는 궁극적으로 **경험(experience)**으로부터 **자동으로 습득(learned)**되어야 하며,
   **사전에 프로그래밍(programmed)**되는 경우가 있더라도,
   이는 **극히 제한된 선천적 프로그램(innate programs)**에만 해당됩니다.

이러한 특성 때문에, **인지 아키텍처는 컴퓨터 아키텍처처럼 언어(language)를 유도**하지만,
그 언어는 어디까지나 **지식(knowledge)**과 **기술(skills)**이라는 형태로
**학습 가능한 지능적 행동(learnable intelligent behavior)**을 산출하는 데 목적을 둡니다.

이 점이 바로 인지 아키텍처와
**임의의 범용 프로그래밍 언어(arbitrary — yet potentially useful — programming language)**를 구분 짓는 결정적 요소입니다.

---

이러한 공통된 기원으로부터, **인지 아키텍처(cognitive architecture)**라는 개념은 여러 하위 분야(subfields)에서 서로 다른 목표에 따라 구체화되었습니다.

* **인지 심리학(cognitive psychology)**에서는,
  ACT-R, Clarion, LIDA (Franklin and Patterson 2006)와 같은 아키텍처들이,
  **기억(memory)**, **문제 해결(problem-solving)**, **지각-운동 상호작용(perceptual-motor interaction)**을 포함한 **통제된 실험에서의 정량적 행동 데이터(quantitative behavioral data)**를 설명하려 시도합니다.

* **인공지능(artificial intelligence)** 분야에서는,
  Soar, Sigma와 같은 아키텍처들이
  **기능적 능력(functional capabilities)** 개발 및
  이를 **자연어 처리(natural language processing)**,
  **시뮬레이션 내 지능형 에이전트(control of intelligent agents in simulations)**,
  **가상 인간(virtual humans)**,
  **실체를 가진 로봇(embodied robots)** 등에 적용하는 데 중점을 둡니다.

* **신경과학(neuroscience)** 분야에서는,
  Leabra (O’Reilly, Hazy, and Herd 2016), Spaun (Eliasmith 2013) 등의 아키텍처가
  인간 두뇌와의 **기계적 유사성(mechanistic compatibility)**을 고려한 구조 및 메커니즘을 채택하며,
  주로 **단순한 기억 및 의사결정 과제(simple memory and decision-making tasks)**에 적용됩니다.

* **로보틱스(robotics)** 분야에서는,
  4D/RCS (Albus 2002), DIARC (Schermerhorn et al. 2006) 등의 아키텍처들이
  **물리적 로봇의 실시간 제어(real-time control of physical robots)**를 주요 과제로 삼습니다.

---

그러나 역사적으로 볼 때, **이들 전문 분야 간 또는 분야 내부에서조차도**,
**인지 아키텍처의 전체적 성격과 구조(the overall nature and shape of this architecture)**에 대한 **합의(agreement)**는 거의 존재하지 않았습니다.

이러한 합의 부족은 다음과 같은 문제들을 초래했습니다:

* 아키텍처 간의 **비교(comparison)** 및 **협업(collaboration)**을 어렵게 만들었고,
* 각 학문 분야에서 제기된 **제약 조건들(constraints)**의 **통합(integration)**을 방해했으며,
* 마음의 개별 구성 요소에 대한 연구에 있어서도 **구조적 지침(guidance)**을 제공하지 못했습니다.

심지어 지금까지도 **우리가 무엇을 만들고 있는지에 대한 통일된 명칭(a unified term)**조차 존재하지 않습니다.
즉, 같은 개념을 지칭하면서도, 다음과 같은 다양한 명칭들이 병용되고 있습니다:

* **인지 아키텍처(cognitive architectures)** — 주로 인지과학(cognitive science)에서 유래한 용어
* **지능형 에이전트를 위한 아키텍처(architectures for intelligent agents)**
* **지능형/인지적 로봇(intelligent/cognitive robots)**
* **가상 인간(virtual humans)**
* **범용 인공지능(artificial general intelligence)**

이러한 명칭들은 각각 **상호작용(interaction)**,
**물리적 인공 신체의 제어(control of artificial physical bodies)**,
**가상 존재의 제어(control of artificial virtual bodies)**,
**도메인 전반에 걸친 일반성(generality across domains)** 등
서로 다른 목표와 요구사항을 함축하고 있습니다.

그럼에도 불구하고, 이러한 서로 다른 흐름들 중에서 **인간 유사(humanlike)** 요소들이
**행동적(behavioral)**, **기능적(functional)**, **신경적(neural)** 제약 조건에 따라
다시 **수렴(reconverge)**할 수 있다면, 이는 **표준 모델(standard model)**이 가능하다는 강력한 신호가 될 수 있습니다.

---

이러한 여러 흐름들을 다시 하나로 모으려는 최근의 시도 중 하나는,
**“인간 유사 인지를 위한 일반 아키텍처(generic architecture for humanlike cognition)”**를 개발하고자 한 작업이었습니다
(Goertzel, Pennachin, and Geisweiller 2014a).

이 노력은 다음과 같은 다양한 아키텍처들로부터 핵심 아이디어들을 **개념적으로 통합(conceptually amalgamated)**하였습니다:

* **CogPrime** (Goertzel, Pennachin, and Geisweiller 2014b)
* **CogAff** (Sloman 2001)
* **LIDA**
* **MicroPsi** (Bach 2009)
* **4D/RCS**
* 그리고 하나의 **딥러닝 형태(deep learning)** (Arel, Rose, and Coop 2009)

이 시도의 여러 목표는 본 논문에서 제안하는 **표준 모델(standard model)**의 목표와 유사하였지만,
그 결과물은 **합의(consensus)**를 반영하기보다는,
다양한 아키텍처로부터 **이질적인 조각(disparate pieces)**들을 **조립한 콜라주(pastiche)**에 가까웠습니다.

즉, 이 시도는 **공통된 요소의 식별(identifying what is common)**보다는
**포괄성(completeness)**을 우선시한 접근이었으며,
그로 인해 진정한 의미의 통합 모델이라기보다는 **누더기식 구성물**에 더 가까웠습니다.

---

본 논문에서 개발한 **표준 모델(standard model)**은,
다음의 세 가지 아키텍처 및 그와 연관된 연구 프로그램에 기반을 두고 있습니다:

* **ACT-R**
* **Soar**
* **Sigma**

이 중 처음 두 아키텍처는, 현재까지 존재하는 아키텍처 중 가장 **완성도가 높고(most complete)**,
**오랜 역사를 지녔으며(long-standing)**,
**가장 폭넓게 응용(widely applied)**되어온 것들입니다.

* **ACT-R**은 **인지과학(cognitive science)** 내에서 시작되었지만,
  이후 **인공지능(artificial intelligence)** 분야로도 확장되었고 (예: Sanner et al. \[2000]),
  **인간 두뇌의 특정 영역들과의 매핑(mapping to brain regions)**도 이루어졌습니다 (Anderson 2007).
  이를 통해 ACT-R은 **Leabra 신경 아키텍처**와 통합되었고 (Jilk et al. 2008),
  **로봇 제어(robot control)**에도 사용되었습니다 (예: Kennedy et al. \[2007]).

* **Soar**는 반대로 **인공지능 분야**에서 시작되었으며 (Newell 1990),
  이후 **인지과학 영역**으로 확장되었고,
  마찬가지로 **로봇 제어**에도 적용되었습니다 (Laird and Rosenbloom 1990; Laird et al. 2012).

* **Sigma**는 이 두 아키텍처로부터 얻은 교훈을 바탕으로 보다 최근에 개발된 아키텍처입니다.
  이 또한 인공지능에서 출발하였으나, 점차 **인지과학과의 연계**를 시도하고 있습니다 (예: Rosenbloom \[2014]).
  Sigma는 **그래프 기반 모델(graphical models)**에 기반하고 있으며,
  최근에는 여기에 **신경망(neural networks)**까지 확장하여 통합하였습니다 (Rosenbloom, Demski, and Ustun 2016b).
  또한 **가상 인간(virtual humans)**의 제어에도 사용된 바 있습니다 (Ustun and Rosenbloom 2016).

---

우리가 이 세 가지 아키텍처를 선택한 이유는, **우리가 이 아키텍처들을 잘 알고 있기 때문**입니다.

물론, **표준 모델(standard model)**의 궁극적인 목표는
더 많은 아키텍처들과 연구 프로그램들에 기반을 두는 것입니다.
하지만 우리의 경험상, **해당 아키텍처 또는 연구 프로그램에 정통한 전문가가 직접 참여하지 않는 한**,
그 결과는 유용하기보다는 오히려 **문제를 야기할 가능성**이 더 큽니다.

따라서, 우리는 다른 아키텍처들에 대한 분석은 **전문가들이 직접 참여할 수 있을 때까지**
— 예컨대 **전문 심포지엄(symposium)**이나 **워크숍(workshop)**을 통해 —
**일단 보류**하기로 결정했습니다.

그 이후에는 보다 **장기적이고 포괄적인 논문(longer and more comprehensive article)**으로 발전시키는 것을 목표로 하고 있습니다.

그럼에도 불구하고, 이 세 가지 아키텍처만으로도
이미 **인공지능(artificial intelligence)**과 **인지과학(cognitive science)**을 넓게 포괄하고 있으며,
여기에 더해
**신경과학(neuroscience)**과 **로보틱스(robotics)**,
그리고 **가상 인간(virtual humans)**에까지 확장되고 있다는 점은 중요합니다.

다만 분명히 해두어야 할 것은,
이 세 아키텍처 중 어느 것도 **신경과학이나 로보틱스 분야에서 직접 기원한 것은 아니다**라는 사실입니다.

---

### 세 가지 인지 아키텍처 (Three Cognitive Architectures)

앞 절에서는 **인지 아키텍처(cognitive architecture)**의 일반 개념을 소개했습니다. 이제부터는, 본 논문이 **표준 모델(standard model)**의 초기 합의를 **확장**하는 데 초점을 맞추었던 **세 가지 특정 아키텍처**를 소개합니다.

각 아키텍처는 **자체적인 용어 체계(their own terms)**로 설명되며,
해당 아키텍처의 구조를 **시각적으로 나타내는 그림(figure)**도 함께 제시됩니다.

이 그림들 간의 **공통점을 부각시키기 위한 수정**은 따로 이루어지지 않았습니다. 예를 들어:

* Soar 도식에서는 **학습 메커니즘(learning mechanisms)**이 명시적으로 표현되어 있지만,
  나머지 두 아키텍처에서는 그렇지 않습니다.

다만, 모든 아키텍처 그림에서 **구성 요소별 색상(color scheme)**만은 통일하여 표시하였습니다.
색상과 의미는 다음과 같습니다:

* 갈색(brown): **작업 기억(working memory)**
* 빨간색(red): **명시적 기억(declarative memory)**
* 파란색(blue): **절차적 기억(procedural memory)**
* 노란색(yellow): **지각(perception)**
* 녹색(green): **운동(motor)**

이후의 표준 모델 설명에서는 이들 아키텍처 간의 **공통점 식별 작업(identifying commonalities)**이 핵심적으로 다루어질 것입니다.

---

**ACT-R**은 여러 개의 모듈(modules)로 구성되어 있으며,
이 모듈들은 **비동기적(asynchronously)**이고 **병렬적(parallel)**으로 작동합니다.
이 모듈들은 중앙에 위치한 **규칙 기반의 절차적 모듈(rule-based procedural module)**을 중심으로 연결되어 있으며,
이 모듈이 **전체 시스템의 전역 제어(global control)**를 담당합니다 (그림 1 참조).

각 모듈 내에서는 **상당히 높은 수준의 병렬 처리(parallel processing)**가 이루어질 수 있지만,
각 작업(operation)은 **단일한 결과(single result)**만을 생성하며,
이 결과는 해당 모듈에 고유한 **작업 기억 버퍼(module-specific working memory buffer)**에 저장됩니다.

이러한 버퍼는 **절차적 모듈(procedural module)**의 조건부 규칙에서 검사할 수 있으며,
다른 모듈로 전송되어 해당 모듈의 동작을 유도할 수도 있습니다.
즉, **모듈 간 상호작용(inter-module interaction)**은
이러한 **작업 기억 버퍼(buffer)**들을 통해 이루어집니다.

---

**Soar** 역시 **비동기적(asynchronous)**이고 **내부적으로 병렬적(internally parallel)**인 여러 모듈로 구성되어 있습니다 (그림 2 참조).
하지만 Soar에서는 이들 모듈이 **공유되는 단일 작업 기억(single shared working memory)**에
모두 직접적으로 연결되어 있다는 점에서 ACT-R과 다릅니다.

Soar에서의 제어(control)는 다음과 같이 수행됩니다:

* **규칙 기반의 절차적 기억(rule-based procedural memory)**에 저장된
  **규칙들(productions)**이 **작업 기억(working memory)**을 조건으로 감시(condition on),
* 적용이 가능한 규칙들이 있을 경우,
  그 중 일부가 **동시에 작동(fire simultaneously)**하여 작업 기억을 갱신(update)합니다.

이러한 규칙들은 다음을 포함합니다:

* **유지 유지 규칙(maintenance rules)**: 작업 기억을 유지하거나 갱신
* **탐색 규칙(search rules)**: 문제 해결을 위한 다음 단계 생성
* **기타 다양한 인지 기능을 구현하는 규칙들**

모든 추론은 **문제 공간(problem spaces)** 내에서 **목표 지향(goal-directed)** 방식으로 발생하며,
이를 통해 Soar는 **하위 목표(subgoals)**와 **계층적 행동(hierarchical behavior)**을 자연스럽게 생성합니다.

Soar는 또한 **절차적 기억(procedural memory)** 외에,
**일화적 기억(episodic memory)**과 **语义 기억(semantic memory)**을
개별 모듈로 보유하고 있으며,
각각이 작업 기억과 상호작용합니다.

---

**Sigma**는 **단일 작업 기억(single working memory)**에 기반한다는 점에서 **Soar**와 유사하지만,
그 구현 방식은 매우 다릅니다 (그림 3 참조).

Sigma는 **결합된 수학적 기반(common mathematical foundation)**에 의해 정의되는
**다양한 형태의 기억과 처리 메커니즘**을 모두 통합하려는
보다 근본적인 시도를 담고 있습니다.
이 수학적 기반은 **혼합형 확률 그래프 모델(hybrid probabilistic graphical models)**로,
이들은 **총합-곱(sum–product)** 계산 과정을 통해 **근사 추론(approximate inference)**을 수행합니다.

Sigma의 구조적 요소들은 다음과 같은 방식으로 작동합니다:

* **작업 기억(working memory)**은 **요소들(terms)**의 집합으로 구성되며,
  각 요소는 **변수(variable)**, **상수(constant)**, 또는 이들의 **함수 적용(function application)** 형태입니다.

* 이러한 요소들은 **인간이 가진 기억 유형들** — 예를 들어 **절차적(procedural)**,
  **일화적(episodic)**, **语义(semantic)** — 로 구분되는
  **기억 모듈(memory modules)** 내에 존재합니다.

* 각 모듈은 자체적인 **확률 모델(probabilistic model)**을 기반으로 하며,
  이들은 **전역 그래프(global graph)** 내에서 연결되어 **정보 전달 및 추론(information flow and inference)**이 가능해집니다.

Sigma는 또한 **정확한 확률 계산(exact probability calculation)**이 아닌
**근사 추론(approximate inference)**에 중점을 둠으로써,
복잡한 문제를 효율적으로 해결할 수 있도록 설계되어 있습니다.

---

이 세 아키텍처는 여러 측면에서 **명백히 서로 다르며(clearly differ)**,
그 차이는 단순히 **표현 방식 또는 구현 방식(style or implementation)**에만 국한되지 않습니다.

예를 들어:

* **ACT-R**은 **모듈(module)** 중심 구조이며,
  각 모듈은 자체 **작업 기억 버퍼(working memory buffer)**를 갖고 있어
  모듈 간 **정보 흐름(information flow)**이 보다 **제한적(constrained)**입니다.

* 반면 **Soar**와 **Sigma**는 **공유 작업 기억(shared working memory)**을 사용하며,
  이 구조는 보다 **자유로운 상호작용(interaction)**과 **정보 공유**를 가능하게 합니다.

또한, 이 세 아키텍처는 **지식 표현(knowledge representation)** 방식에서도 다릅니다:

* **ACT-R**과 **Soar**는 모두 **기호 기반(symbolic)** 시스템으로서,
  규칙(rules)과 조건(condition)에 의해 구동됩니다.

* 반면 **Sigma**는 **하이브리드 확률 모델(hybrid probabilistic model)**을 기반으로 하며,
  이는 **연속성(continuity)**과 **불확실성(uncertainty)**을 자연스럽게 처리할 수 있도록 설계되어 있습니다.

이러한 차이점에도 불구하고, 이 세 아키텍처는 다음과 같은 **중요한 공통 요소(common elements)**들을 공유합니다:

* **작업 기억(working memory)**,
* **절차적 기억(procedural memory)**,
* **명시적 기억(declarative memory)**,
* **지각(perception)**,
* **운동 제어(motor control)**,
* **학습 메커니즘(learning mechanisms)**,
* 그리고 **행동의 계층적 조직 구조(hierarchical organization of behavior)** 등입니다.

이러한 공통 요소들이 바로 우리가 이후에 논의할 **표준 모델(standard model)**의 **핵심 기반(core basis)**이 됩니다.

---

### 표준 모델을 향하여 (Toward a Standard Model)

**표준 모델(standard model)**의 목적은 다음과 같습니다:

* **기존 아키텍처들의 공통된 기반(common basis)**을 명시적으로 밝히고,
* 그것을 **공유된 체계적 프레임워크(shared systematic framework)**로 공식화하며,
* 더 나아가 **인지 아키텍처(cognitive architecture)**의 발전을 위한
  **공동의 목표(common goal)**를 제공하는 것입니다.

이러한 표준 모델은,
ACT-R, Soar, Sigma의 세 아키텍처가 **공통적으로 구현하고 있는 기능 및 구조**에 대해
**초기 합의(initial consensus)**에 근거하여 정의됩니다.

보다 구체적으로는 다음의 5가지 구성 요소로 설명됩니다:

1. **처리 단위(Processing Units)**:
   지각(perception), 작업 기억(working memory), 절차적 기억(procedural memory), 명시적 기억(declarative memory), 운동(motor) 등

2. **기능적 시스템 조직(Functional System Organization)**:
   각 처리 단위 간의 정보 흐름 및 제어 구조

3. **지식 표현(Representations)**:
   개념, 사실, 규칙 등을 나타내는 형식(formalism)

4. **학습과 적응(Learning and Adaptation)**:
   경험에 기반한 지식과 행동의 변화 메커니즘

5. **행동의 생성 및 구조화(Behavior Generation and Structuring)**:
   목표 지향적 행동의 생성, 하위 목표 구조, 탐색 전략 등

이러한 구성 요소는 **서로 분리된 모듈(modules)**로 이해될 수 있지만,
실제로는 **상호작용하는 통합 시스템(interacting integrated system)**으로 작동합니다.

---

세 아키텍처 모두 **유사한 유형의 지식(same kinds of knowledge)**에 대한 **표현 구조(representations)**를 포함하고 있지만,
이러한 표현은 각기 **서로 다른 방식으로 구현(different ways of implementing)**되어 있습니다.

예를 들어:

* **ACT-R**과 **Soar**는 모두 **기호 기반(symbolic)** 표현 체계를 사용합니다.
  하지만 Soar는 **슬롯-값 구조(slot–value structures)**를 사용하고,
  ACT-R은 **청크(chunk)**라는 단위를 통해 정보를 조직합니다.

* 반면 **Sigma**는 **확률적 표현(probabilistic representations)**을 사용하여,
  기호 구조와 수치적 추론(numeric inference)을 통합합니다.
  이는 개념 간 **연속적인 관계(continuous relationships)**를 다룰 수 있게 합니다.

또한, 세 아키텍처는 모두 다음의 **핵심 처리 체계**를 포함하고 있습니다:

1. **지각(perception)**: 외부 세계로부터의 입력을 해석하고 내적 표현으로 변환
2. **운동(motor)**: 행동 명령을 외부 세계에 전달
3. **작업 기억(working memory)**: 현재 활성화된 정보들을 유지하며,
   추론과 행동 생성에 사용
4. **절차적 기억(procedural memory)**: 조건–행동 규칙 또는 그에 상응하는 구조를 포함하며,
   이는 **행동을 유도(drives behavior)**하고 작업 기억을 수정
5. **명시적 기억(declarative memory)**: 사실적 지식(semantic)이나 에피소드적 정보(episodic)를 저장

이러한 구성 요소들은 **모든 인간 유사 인지 시스템(humanlike cognitive system)**이
공통적으로 갖추어야 하는 **기본 처리 요소(basic processing elements)**로 간주됩니다.

---

이러한 **처리 구성 요소들(processing components)** 각각은
**인간 수준의 인지 능력(human-level cognitive capabilities)**의 전체 범위를 생성하기 위해 **필수적(necessary)**입니다.

예를 들어:

* **지각(perception)**과 **운동(motor)** 구성 요소는
  **외부 세계와의 상호작용(interaction with the external world)**을 가능하게 합니다.

* **작업 기억(working memory)**은
  **현재 활성화된 정보(currently active information)**를 유지하며,
  이는 대부분의 인지 처리(cognitive processing)에 중심 역할을 합니다.

* **절차적 기억(procedural memory)**은
  **조건-행동 규칙(condition–action rules)**을 기반으로
  **추론(reasoning)**과 **행동 선택(action selection)**을 수행합니다.

* **명시적 기억(declarative memory)**은
  **지식(knowledge)**과 **경험(experience)**을 저장하여,
  **학습(learning)**과 **회상(recall)**, **추론(reasoning)**의 기반을 제공합니다.

이러한 구성 요소들은 또한 **서로 밀접하게 상호작용(tightly interact)**합니다.

예를 들어:

* **절차적 기억**은 **작업 기억**을 조건으로 사용하여
  어떤 행동을 취할지를 결정하며, 그 결과 **작업 기억을 갱신(update)**합니다.

* **작업 기억**은 또 다른 구성 요소인
  **명시적 기억**이나 **지각**, **운동 체계**와도 상호작용합니다.

이와 같이, **표준 모델(Standard Model)**은
인간 수준의 인지에서 필요한 **핵심 처리 구성 요소들과 그 상호작용 구조(interaction structure)**를
공통의 기반으로 제시하고자 합니다.

---

**표준 모델(Standard Model)**은 단순히 **구성 요소들의 집합(set of components)** 그 이상입니다.
이 모델은 **그 구성 요소들이 어떻게 함께 작동하는지(how they work together)**에 대한 **구조적 제약(structural constraints)**도 포함합니다.

이러한 제약은 다음을 포함합니다:

* 어떤 정보가 어떤 구성 요소들 사이를 오갈 수 있는지에 대한 **정보 흐름 경로(information flow paths)**
* 어떤 구성 요소가 **행동 제어(control of behavior)**를 주도하는지
* **기억 인출(memory retrieval)**, **학습(learning)**, **추론(reasoning)** 등 주요 과정의 **시간적 특성(temporal characteristics)**
* 그리고 구성 요소 간 **우선순위(priority)** 또는 **의존성 관계(dependencies)**

이러한 구조적 제약은
**통합된 전체 시스템(fully integrated system)**을 정의하며,
이를 통해 단순히 부품들의 모음이 아닌 **기능적으로 작동하는 인지 시스템(functional cognitive system)**을 가능하게 합니다.

요약하자면, 표준 모델은 다음 두 가지를 함께 제공합니다:

1. **처리 구성 요소들(processing components)**
2. 그들 간의 **조직화된 상호작용 방식(organized pattern of interaction)**

이 모델은 특정 구현체에 고정되지 않으며,
여러 아키텍처와 시스템에 **응용 가능(applicable)**한 **상위 수준의 추상 모델(high-level abstract model)**로 기능합니다.

---

### 왜 표준 모델이 필요한가 (Why a Standard Model Is Needed)

**표준 모델(Standard Model)**은 단지 **기존 아키텍처들로부터의 귀납(induction)**을 통해
무엇이 일반적으로 나타나는지를 정리하는 데 그치지 않습니다.
그보다는, 다음과 같은 다섯 가지 목적을 위해 **의도적으로 개발(intentionally developed)**된 것입니다.

---

**1. 공통된 기반 제공 (Provide a Common Framework)**

표준 모델은, 다양한 분야에 걸쳐 존재하는
**지능 시스템(intelligent systems)** 연구를 위한
**공통 언어(common language)**와 **참조 프레임(reference frame)**을 제공합니다.
이는 서로 다른 접근 방식 간 **비교(comparison)**와 **통합(integration)**을 가능하게 하며,
상호 이해를 증진시킵니다.

---

**2. 아키텍처 설계 지침 (Guide Architecture Development)**

표준 모델은 새로운 인지 아키텍처를 설계할 때
**핵심 구성 요소와 구조(core components and structures)**를 명확히 제시함으로써,
**설계(design)**의 방향성을 제공합니다.
이는 **불완전하거나 단편적인 구현(weak or fragmented implementations)**을 방지하고,
보다 **완성도 높은 시스템(complete systems)**의 개발을 장려합니다.

---

**3. 경험적 평가 기준 (Support Empirical Evaluation)**

표준 모델은 인지 아키텍처의 구현이
**기능적(functional)**, **행동적(behavioral)**, **신경적(neural)** 제약 조건을
얼마나 잘 충족하는지를 평가할 수 있는 **기준(benchmark)**을 제공합니다.
즉, **어떤 요소가 누락되었는가** 또는
**어떤 구성 방식이 제한적 혹은 과도한가**를 진단할 수 있게 해줍니다.

---

**4. 다학제 간 협력 촉진 (Facilitate Cross-Disciplinary Collaboration)**

표준 모델은 인공지능, 인지과학, 신경과학, 로보틱스 등
**서로 다른 분야(different disciplines)** 사이의 **지식 공유(knowledge sharing)**를 촉진합니다.
이는 **하나의 학문 분야에서의 발견(discoveries)**이
다른 분야의 모델이나 시스템 설계에 **직접적인 영향을 미칠 수 있도록** 해줍니다.

---

**5. 인간 인지 이해의 통합 (Unify Understanding of Human Cognition)**

궁극적으로, 표준 모델은 인간의 **지각(perception)**, **기억(memory)**, **학습(learning)**, **추론(reasoning)**,
**계획(planning)**, **언어(language)**, **운동 행동(motor behavior)** 등을
**단일 체계(single framework)** 내에서 설명할 수 있는 **통합 모델(integrated model)**로 기능할 수 있습니다.
이는 인간 수준의 인공지능을 구현하려는 시도뿐만 아니라,
**인간 인지 자체에 대한 과학적 이해(scientific understanding of cognition)**에도 기여할 수 있습니다.

---

### 결론 (Conclusions)

본 논문은 **표준 모델(Standard Model)**의 개념을 제안하며,
이는 **인공지능(Artificial Intelligence)**, **인지과학(Cognitive Science)**,
**신경과학(Neuroscience)**, 그리고 **로보틱스(Robotics)**를 아우르는
**공통된 계산적 프레임워크(common computational framework)**로 기능할 수 있습니다.

이 모델은 다음을 바탕으로 합니다:

* 세 가지 인지 아키텍처 (ACT-R, Soar, Sigma) 간의 **공통점 식별(identification of commonalities)**
* 그리고 이들로부터 도출한 **초기 합의 기반(initial consensus base)**

우리는 표준 모델이 다음과 같은 방식으로 유용할 것이라 기대합니다:

1. **지능 시스템 설계(designing intelligent systems)**의 지침 제공
2. **다학제 간 연구(cross-disciplinary research)**의 통합 기반 형성
3. **인간 인지(human cognition)**에 대한 이론적, 실용적 이해 증진

표준 모델은 다음과 같은 다섯 가지 주요 처리 구성 요소를 중심으로 구성됩니다:

* **작업 기억(working memory)**
* **절차적 기억(procedural memory)**
* **명시적 기억(declarative memory)**
* **지각(perception)**
* **운동 제어(motor control)**

이러한 구성 요소들은 **통합된 구조적 제약(integrated structural constraints)** 속에서
상호작용하며, 인간 수준의 지능을 위한 기반을 이룹니다.

이 모델은 **고정된 구현체(fixed implementation)**가 아니며,
대신 다양한 구현과 응용을 위한 **상위 수준의 추상 모델(high-level abstract model)**로 작동합니다.

우리는 향후 다음과 같은 방향으로 발전이 이루어지길 기대합니다:

* 보다 **넓은 아키텍처 집합(wider set of architectures)**에 대한 분석 포함
* 다양한 학문 분야에서의 **비판적 평가 및 실험적 검증(empirical validation)**
* 그리고 **실제 시스템(real systems)**에의 응용을 통한 효과성 평가

표준 모델은 단순한 이론적 제안이 아니라,
**지능의 과학적 이해(scientific understanding of intelligence)**와
그 **실현(realization)** 모두를 위한 **공통의 기반(common foundation)**이 되기를 목표로 합니다.

---

표 1. 표준 모델 아키텍처의 기본 가정

다음은 인지 아키텍처에 대한 기술적 설명의 한국어 번역이며, 모든 전문용어는 괄호로 병기하였습니다.

---

### A. 구조 및 처리 (Structure and Processing)

1. 아키텍처 처리의 목적은 **최적성(optimality)**이 아니라 **제한된 합리성(bounded rationality)**을 지원하는 것이다.
2. 처리는 **작업(task)에 독립적인 소수의 모듈**에 기반한다.
3. 아키텍처 처리에는 **상당한 병렬성(parallelism)**이 존재한다.
   a. **모듈 간 병렬 처리(parallel across modules)**
       i. **ACT-R** 및 **Soar**는 *비동기적(asynchronous)*, **Sigma**는 **동기적(synchronous)**이다.
   b. **모듈 내부 병렬 처리(parallel within modules)**
       i. **ACT-R**: 규칙 일치(rule match), **Sigma**: 그래프 해법(graph solution), **Soar**: 규칙 발화(rule firings)
4. **행동(behavior)**은 약 50밀리초(ms) 주기로 작동하는 **인지 사이클(cognitive cycle)**을 통해 **순차적 행동 선택(sequential action selection)**에 의해 주도된다.
5. 복잡한 행동은 전역 최적화(global optimization) 또는 계획(planning)을 위한 별도의 아키텍처 모듈 없이, **지역(context) 내에서 독립적으로 작동하는 인지 사이클의 연속**으로부터 발생한다.

---

### B. 기억과 내용 (Memory and Content)

1. **선언적(declarative)** 및 **절차적(procedural)** 장기 기억(long-term memory)은 **기호 구조(symbol structures)**와 **관련된 정량적 메타데이터(quantitative metadata)**를 포함한다.
   a. **ACT-R**: 활성화(activation)를 가진 청크(chunk)와 효용성(utility)을 가진 규칙(rule)
       **Sigma**: 함수(function)를 가진 술어(predicate) 및 조건문(conditional)
       **Soar**: 활성화가 부여된 삼중항(triple)과 효용성이 있는 규칙
2. **전역적 소통(global communication)**은 모든 인지, 지각, 운동 모듈 간 **단기 작업 기억(working memory)**에 의해 제공된다.
3. **전역적 제어(global control)**는 **절차적 장기 기억(procedural long-term memory)**에 의해 제공된다.
   a. 조건(condition)과 행동(action)으로 이루어진 **규칙형(rule-like)** 구조로 구성됨
   b. **작업 기억의 내용을 변화시킴으로써 제어**를 수행함
4. **사실 지식(factual knowledge)**은 **선언적 장기 기억(declarative long-term memory)**에 의해 제공된다.
   a. **ACT-R**: 단일 선언적 기억
       **Sigma**: 절차적 기억과 통합됨
       **Soar**: 의미 기억(semantic memory)과 일화 기억(episodic memory)

---

### C. 학습 (Learning)

1. 기호 구조든 정량적 메타데이터든 **모든 형태의 장기 기억 내용은 학습 가능**하다.
2. 학습은 **온라인(online) 및 점진적(incremental)**으로 일어나며, **수행(performance)의 부산물(side effect)**로 발생한다.
   종종 **수행의 정보 흐름을 역으로 따라가는 방식**으로 이루어진다.
3. **절차적 학습(procedural learning)**은 최소한 **강화 학습(reinforcement learning)**과 **절차적 구성(procedural composition)**을 포함한다.
   a. 강화 학습은 **행동 선택(action selection)**에 대한 **가중치(weight)**를 학습한다.
   b. 절차적 구성은 **행동 자동화(behavioral automatization)**를 만든다.
       i. **ACT-R**: 규칙 구성(rule composition)
       **Sigma**: 개발 중
       **Soar**: 청킹(chunking)
4. **선언적 학습(declarative learning)**은 **사실(fact)**의 획득과 **그 메타데이터의 조정(tuning)**을 포함한다.
5. **보다 복잡한 학습 형태**는 **정해진 소수의 단순 학습 형태의 조합**으로 구성된다.

---

### D. 지각 및 운동 (Perception and Motor)

1. **지각(perception)**은 **특정 작업 기억 버퍼(working memory buffer)**에 **메타데이터가 포함된 기호 구조(symbolic structures)**를 생성한다.
   a. 서로 다른 입력 양식(modality)을 가지며 고유한 버퍼를 가진 **다수의 지각 모듈**이 존재할 수 있다.
   b. **지각 학습(perceptual learning)**은 **새로운 패턴을 학습하고 기존 패턴을 조정(tuning)**한다.
   c. **주의 병목(attentional bottleneck)**은 작업 기억에 들어올 수 있는 정보의 양을 제한한다.
   d. 지각은 **작업 기억으로부터의 상향(top-down) 정보에 의해 영향받을 수 있다.**
2. **운동 제어(motor control)**는 **자기 버퍼 내의 기호 관계 구조(symbolic relational structures)**를 **외부 행동(external actions)**으로 변환한다.
   a. 지각과 마찬가지로, **다수의 운동 모듈**이 존재할 수 있다.
   b. **운동 학습(motor learning)**은 **새로운 행동 패턴을 학습하고 기존 행동을 조정(tuning)**한다.

---
