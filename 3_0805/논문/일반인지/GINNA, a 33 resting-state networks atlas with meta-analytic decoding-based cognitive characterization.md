**"GINNA, a 33 resting-state networks atlas with meta-analytic decoding-based cognitive characterization"**
---

### 초록 (Abstract)

자발적 안정상태 네트워크(resting-state networks, RSNs)는 자기공명영상(magnetic resonance imaging, MRI)을 통해 처음 관찰된 이래로, 이들의 **인지적 관련성(cognitive relevance)**은 지속적으로 제기되어 왔습니다. 그러나 현재까지 이러한 네트워크의 **경험적 인지 특성화(empirical cognitive characterization)**는 제한적이었습니다. 본 연구는 **Groupe d’Imagerie Neurofonctionnelle Network Atlas (GINNA)**를 소개합니다. 이는 33개의 안정상태 네트워크로 구성된 **포괄적 뇌 아틀라스(comprehensive brain atlas)**입니다.

이 아틀라스는 **1812명 참가자의 안정상태 데이터(resting-state data)**를 기반으로, **개별적으로 추출된 독립 성분들(independent components)**을 분류하여 구성되었으며, 개인 간 일관된 탐지(consistency of detection between subjects)를 보장합니다. 우리는 각 GINNA 네트워크의 인지적 관련성을 **Neurosynth 기반의 메타분석 디코딩(meta-analytic decoding)**과 **생성적 영가설 검정(generative null hypothesis testing)**을 통해 추가로 탐색하였습니다.

각 네트워크에 대해 통계적으로 유의한 인지 용어들을 도출한 후, **6명의 저자 간 합의(consensus)**를 통해 적절한 **인지 과정(cognitive processes)**으로 통합하였습니다. GINNA 아틀라스는 **다양한 형태학적(topological) 특성**을 나타내며, 인간의 알려진 **인지적 레퍼토리(cognitive repertoire)**의 광범위한 스펙트럼을 반영합니다. 각 네트워크에 연결된 인지 과정들은 **Cognitive Atlas 온톨로지(Cognitive Atlas ontology)**의 표준 명명법을 따르고 있어, 이후의 **경험적 검증(empirical validation)**을 위한 기회를 제공합니다.

---

### 서론 (Introduction)

뇌는 본질적으로 **서로 밀접하게 연결된 뇌 영역(brain regions)** 또는 **네트워크(networks)**로 구성되어 있습니다. **안정상태 기능적 자기공명영상(resting-state functional magnetic resonance imaging, rs-fMRI)**을 이용하면, 먼 거리의 뇌 영역들 간에 **혈중 산소 수준 의존 신호(blood oxygen level-dependent, BOLD signal)**의 저주파 자발적 변동(low-frequency spontaneous fluctuations)이 동기화되어 있다는 것이 관찰됩니다【1】.

이러한 소위 **안정상태 네트워크(resting-state networks, RSNs)**의 기능적 역할을 이해하는 것은 **인지신경과학(cognitive neuroscience)**의 핵심 목표로 남아 있습니다. 분산된(distributed) 뇌 영역들의 **조정된 활동(coordinated activity)**이 **인지(cognition)**를 지원한다는 주장은 오래전부터 제기되어 왔습니다【2–4】.

RSNs이 처음 관찰된 이후, 이들은 종종 **과제 기반 네트워크(task-based networks)**에서 관찰되는 주요 인지 시스템의 경계를 반영하는 방식으로 구성되어 있다는 점이 주목되었습니다—예: **운동감각(somatomotor)**【1】, **시각(vision)**【5】, **일화기억(episodic memory)**【6】, **언어(language)**【7】. 이러한 점은 RSNs이 기능적으로 유의미한 시스템(functionally relevant systems)을 나타낼 수 있다는 가능성을 시사합니다【8–10】.

그러나 일부에서는 네트워크를 **해부학적으로 기반한 분류체계(anatomically grounded taxonomy)**에 따라 명명할 것을 제안한 반면【11】, 실제로는 연구자들이 **추정되는 인지 기능(putative cognitive functions)**을 기준으로 네트워크를 명명하는 경향이 있습니다【12】.

처음에는 안정된 뇌 상태가 본질적으로 **서로 반대되는 두 시스템**—즉 **외적(task-positive)** 시스템과 **내적(task-negative)** 시스템—으로 분리된다고 제안되었습니다【13】. 이후, 이 두 시스템은 다음과 같은 **다섯 개의 모듈(modules)**로 계층적으로 분해될 수 있음이 밝혀졌습니다:

1. **전환/조절(switching/control)**,
2. **감각/운동/주의(sensory/motor/attentional)**,
3. **시각(visual)**,
4. **정보의 조작/유지(manipulation/maintenance of information)**,
5. **자발적 사고(spontaneous thoughts)**의 발생【14】.

현재 가장 널리 사용되는 아틀라스는 기능적 네트워크를 다음과 같이 **7개로 분할(segregation)**합니다:

* 시각(visual)
* 운동감각(somatomotor)
* 등쪽 주의(dorsal attention)
* 배쪽 주의(ventral attention 또는 salience)
* 변연계(limbic)
* 전두두정 조절(frontoparietal control)
* 기본(default) 네트워크【15】.

그러나 RSNs의 기능적 관련성은 대부분 **간접적으로(indirectly)** 제시되어 있습니다. 네트워크의 인지 기능은 **과제 기반 네트워크와의 시각적 유사성(visual similarity)**을 기반으로 추론되는 경우가 많습니다. 하지만 이러한 방식은 **신경영상 전문가들조차도 신뢰성이 낮은 것으로 나타났습니다**【12】. 이처럼 **시각적 유사성 기반 추론은 결과 해석 시 큰 오류 가능성**을 내포하고 있습니다.

또한, 인지 기능과 RSNs 간의 연결성은 반드시 **일대일(one-to-one) 매핑 관계**로 정해져 있지 않다는 주장도 제기되어 왔습니다. 특히, RSN 아틀라스에서 일반적으로 제시되는 **7개 수준의 낮은 세분화도(granularity)**는 이러한 매핑을 더욱 어렵게 만듭니다【16】.

---

그럼에도 불구하고, 다양한 **경험적 증거(empirical evidence)**들은 RSN의 인지적 관련성을 뒷받침해왔습니다. **안정상태 뇌 조직(resting brain organization)**과 **과제 수행 중 뇌 조직(task-engaged brain organization)** 간의 첫 번째 직접적인 연결은 Smith 외(2009)에 의해 제시되었습니다【17】. 이들은 안정 상태에서 **독립 성분 분석(independent component analysis, ICA)**을 통해 추출된 네트워크들이, 동일한 방법으로 **BrainMap 활성화 맵 데이터베이스(BrainMap activation maps database)【18】**에서 추출된 과제 기반 네트워크와 공간적으로 매우 유사하다는 것을 보여주었습니다.

이러한 **시금석 연구(seminal observation)** 이후, 여러 후속 연구들은 안정 상태와 과제 기반 네트워크 구조 간의 연결을 지속적으로 강화해왔습니다. 예를 들어,

* 과제 중에 관찰되는 네트워크 구조는 **안정상태 네트워크 구조에 의해 형성된다(shaped)**는 증거가 제시되었으며【19, 20】,
* 또는 RSN이 **인지 모듈화를 구현한다(cognition modularly implemented)**는 주장도 있습니다【21, 22】.

종합적으로, 이러한 결과들은 **RSNs이 인지를 구성하는 핵심 단위(critical cognitive units)**를 반영할 수 있다는 주장을 지지합니다.

---

**Laird 외(2011)**【23】는 **내재적 연결성 네트워크(intrinsic connectivity networks)**의 인지적 해석에 대한 **포괄적인 설명(extensive description)**을 처음으로 제공하였습니다. 이들은 Smith 외(2009)【17】에서 사용된 것과 동일한 방법론, 즉 **독립 성분 분석(ICA)**을 활용하여 **BrainMap 데이터베이스【18】**로부터 내재적 연결성 네트워크를 추출하였으며, 이러한 해석이 가능했던 것은 해당 데이터베이스에 수록된 **인지 과정(cognitive processes)**에 대한 **수작업 주석(manual annotations)**의 풍부함 덕분이었습니다.

유사한 시도로, 다른 연구에서는 **BrainMap 분류체계(taxonomy)【18】**를 사용하여 네트워크별로 **20개의 인지 영역(cognitive domains)**에 걸친 **기능적 지문(functional fingerprint)**을 추출한 바 있으며(예: “청각-지각(Audition-Perception)”, “기억-인지(Memory-Cognition)”), 이를 통해 각 네트워크의 고유한 인지 프로파일을 밝힐 수 있었습니다【24】.

그러나 이처럼 귀중한 통찰을 제공한 연구들에도 몇 가지 **제한점(limitations)**이 존재합니다. 예를 들어, **과제 기반 연구(task studies)【17, 23】**에서 도출된 네트워크 맵을 분석함으로써 **인지-행동 용어(cognitive-behavioral terminology)**와의 연결은 가능했지만, RSN의 해석은 여전히 **BrainMap 기반 네트워크(즉, 과제 기반 네트워크)**와의 **외형적 유사성(apparent resemblance)**에 의존하고 있었습니다.

이러한 접근은 **위치상의 작은 차이(topological differences)**나 **영역별 활성화 수준(regional activation levels)**의 차이에 따라 **인지적 프로파일(cognitive profile)**에 중대한 차이를 초래할 수 있다는 점에서 **문제의 소지**가 있습니다.

또한, 다른 연구들에서는 각 네트워크의 인지 프로파일을 **20개의 광범위한 행동 영역(broad behavioral domains)【24】**에 따라 정의하기도 하였으나, 이 경우 **세부적인 인지 과정(fine-grained cognitive processes)**을 기술하는 데 한계가 있었습니다.

마지막으로, BrainMap 데이터베이스의 활성화 맵은 **메타데이터 품질(metadata quality)**가 높기는 하지만, 이는 **제한된 연구(subset of studies)**에 대해 **수작업으로 주석된(annotation)** 것으로, **fMRI 문헌 전체**를 포괄하지 못합니다.

반면, **자연어 처리(natural language processing)**에 기반한 **Neurosynth【25】**는 수천 개의 fMRI 활성화 연구로부터 **용어 관련 메타분석 맵(term-related meta-analytic maps)**을 **자동으로 생성**합니다. 따라서 BrainMap과 비교했을 때 **훨씬 광범위하게 확장 가능하며**, **더 구체적인 용어(specific terms)**를 포함할 수 있습니다.

---

최근 들어 Neurosynth의 발전을 바탕으로, **디코딩 방법(decoding methods)**의 새로운 범주가 등장하였습니다. 이 방법들은 특정 **뇌 활동(brain activity)**이 있을 때, 이에 **관여할 가능성이 있는 인지 기능(cognitive functions)**을 탐색하는 데 사용됩니다【26–28】.

이러한 디코딩 방법들은 **메타분석 맵(meta-analytic maps)**과의 공간적 비교(spatial comparison)를 통해 **추정되는 인지 과정(putative cognitive processes)**의 존재를 추론하는 데 활용됩니다. 예를 들어,

* **짧은 과제 기반 fMRI 블록(short task-fMRI blocks)**의 인지적 내용을 추론하거나【29】,
* **인간의 두정이랑(intraparietal sulcus)【30】**의 인지 프로파일을 밝히는 데 성공적으로 사용되었으며,
* **비디오 시청 중 참가자의 인지 상태(cognitive states)【31】**를 밝히는 데에도 활용된 바 있습니다.

이러한 방법들은 RSN의 인지적 관련성을 평가하는 데 있어서도 유용한 가능성을 제시합니다. 구체적으로는, RSN의 **형태(topology)**를 메타분석 맵과 통계적으로 비교함으로써, 그 인지적 관련성을 평가할 수 있게 됩니다.

하지만, 지금까지의 연구들 중에서, **RSN의 인지적 관련성(cognitive relevance of RSNs)**을 규명하기 위해 **메타분석 디코딩(meta-analytic decoding)**을 직접적으로 적용한 사례는 **존재하지 않습니다**.

---

본 연구는 **Groupe d’Imagerie Neurofonctionnelle Network Atlas (GINNA)**를 소개합니다. 이는 각각의 안정상태 네트워크(resting-state network)의 **인지적 관련성(cognitive relevance)**을 경험적으로 특성화한 **정밀한 수준의 33개 네트워크(fine-grained 33 networks)**로 구성된 새로운 아틀라스입니다.

기존의 아틀라스들과 달리, GINNA는 **개인 수준(individual level)**에서 얻어진 **독립 성분들(independent components)**을 분류하는 방식으로 구축되어, **보다 높은 세분화도(finer granularity)**를 제공하며, 개별 피험자들 간에 **구성 요소가 안정적으로 나타남(reliable presence)**을 보장합니다.

각 네트워크에 **인지적 라벨(cognitive label)**을 부여하기 위한 전략은,

* **Neurosynth 데이터베이스에서 수작업으로 선별된 하위 집합(manually curated subset)**으로부터
* **인지 용어(cognitive terms)**를 디코딩(decoding)하여 구축되었습니다.

따라서 본 아틀라스는 현재의 **신경영상 문헌(neuroimaging literature)**에 비추어, 각 네트워크의 **가설적 인지 기능(putative cognitive functions)**을 **포괄적으로 특성화(exhaustive characterization)**한 결과물입니다.

이와 같이, 특정 인지 기능에 대한 **정밀한 특성화(careful characterization)**를 기반으로 구축된 아틀라는,

* **신경망 기능에 대한 직접적/인과적 평가(direct/causal assessments)**를 목표로 하는
* **최신 분석 기법(newly emerging methods)**과 결합될 경우,
* **기제적 설명(mechanistic accounts)**을 밝히는 데 유용한 가이드가 될 수 있습니다.

---

## 결과 (Results)

### GINNA 안정상태 네트워크 (GINNA resting-state networks)

**GINNA 아틀라스(GINNA atlas)**는 \[그림 1 및 그림 2]에 제시되어 있으며, 다음의 주소에서 **공개적으로 이용 가능(publicly available)**합니다:
🔗 [https://github.com/Achillegillig/ginna](https://github.com/Achillegillig/ginna)【32】

**안정상태 네트워크 분해(resting-state network decomposition)** 절차를 통해 총 **41개의 네트워크**가 식별되었습니다. 이 중,

* **뇌 외부와 겹치는 네트워크(venous artifacts 중심)** 7개와
* **뇌간(brainstem)에만 국한된 하나의 네트워크**는
  추가 분석에서 제외되었고, 최종적으로 **33개의 RSN(resting-state networks)**이 분석 대상으로 확정되었습니다.

RSN의 번호 지정(RSN01부터 RSN33까지)은 **식별의 신뢰도(reliability of detection)**를 반영합니다.
즉, 번호가 낮을수록 **더 많은 피험자들에게서 탐지되었음을 의미**하며, 예를 들어:

* **RSN01은 99.94%**의 피험자에게서 탐지되었고,
* **RSN33은 49.59%**의 피험자에게서 탐지되었습니다.

GINNA 아틀라스는 **SPM 회색질 템플릿(SPM gray matter template)**에 의해 정의된 **대뇌 피질(cortex)**의 약 **90%를 커버**합니다 (보조 그림 1 참고).
커버되지 않은 영역은 주로 다음과 같은 위치에 존재합니다:

* **자기감수성 인공물(susceptibility artifacts)**의 영향을 받는 부위 (예: 전두동(frontal sinus) 위의 안와전두피질(orbitofrontal cortex),
  또는 이관(ear canals) 위의 하측 측두엽)
* **위상 인코딩 방향(phase encoding axis)**이 전후축(anterior–posterior axis)으로 설정되어 생긴 왜곡(distortions)

적용된 **왜곡 보정(distortion correction)**은 일부 신호를 회복하였지만,

* 이는 획득된 **k-공간(k-space)**의 범위를 벗어난 영역에서는 완전하지 않아 일부 신호 손실이 여전히 존재했습니다【35】.

분석에서 제외된 6개의 네트워크 중 하나는,

* **안와전두 영역 대부분을 포함**하고 있었으며,
* **환형 구조(annular geometry)**를 갖추었고,
* **뇌외 영역(extracerebral cerebrospinal fluid crown)까지 포함**하고 있었기에,
* 이는 **정상적인 네트워크로 간주되지 않아 제외**되었습니다.

한편, **가장 낮은 탐지율을 보인 RSN33**은

* 전측(anterior) 및 하측(inferior) 측두엽(temporal lobe)의 상당 부분을 포함하고 있었으며,
* 이는 자기감수성 인공물이 **탐지율 감소**에 영향을 미쳤을 가능성을 시사합니다.

---

**성별 균형 하위 샘플(gender-balanced subsample)**(총 1016명, 여성 508명)을 이용하여 **집단 평균 안정상태 네트워크(group-average RSN)** 생성을 재현한 결과,
**원본 GINNA 아틀라스와 거의 완벽하게 일치**하는 것으로 나타났습니다.
이는 **Dice 계수(Dice coefficient)**를 통해 평가되었으며,

* 평균 ± 표준편차는 **0.96 ± 0.01**,
* 범위는 **\[0.92–0.98]**로 보고되었습니다 (보조 그림 2 및 3 참고).

해당 성별 균형 하위 샘플에서, 남성과 여성 간 **연령 차이는 통계적으로 유의하지 않았으며**

* 이변량 t-검정(two-tailed t-test) 결과는 t(1013.48) = 0.305, p = 0.76 이었습니다.

또한, **HCP(Human Connectome Project) 데이터셋【36】**으로부터
성별 균형을 맞춘 **150명 하위 샘플**을 대상으로 GINNA RSN 생성 절차를 다시 적용한 결과,

* **총 32개의 대뇌 피질 RSN 중 28개가 양쪽 데이터셋 모두에서 재현됨**이 확인되었습니다 (보조 그림 4 및 5 참고).

반면, **RSN18, RSN27, RSN31, RSN33**은 HCP 기반 분석에서 **관찰되지 않았으며**,

* 이는 해당 네트워크들이 GINNA 전체 데이터셋에서도 **탐지 빈도가 낮았던 점**과
* HCP 샘플 크기가 더 작았던 점을 반영하는 것으로 보입니다.

---

### 메타분석적 인지 용어 디코딩 (Meta-analytic cognitive terms decoding)

총 **506개의 메타분석 맵(meta-analytic maps)** 중에서, **241개(47.6%)**는 **어떠한 RSN에 대해서도 유의한 디코딩 결과가 나타나지 않았습니다** (보조 그림 6A).

모든 RSN에서 유의미하지 않았던 용어들은,

* 최소 하나의 RSN에 대해 유의하게 디코딩된 맵들과 비교하여,
* **영(0) 값의 수가 더 많은 맵(more null values)**의 특성을 보였습니다 (보조 그림 6B).

또한, **가장 관련성이 낮은 용어들(least associated terms)** — 즉,
어느 RSN과도 **Pearson 상관계수(Pearson r)**가 가장 낮고 **통계적으로 유의하지 않은 용어들**은

* **정서 영역(emotional domain)**에 주로 분포하는 것으로 나타났습니다 (보조 그림 6C).

우리의 디코딩 절차는 **네트워크 당 평균 12개의 용어(terms)**를 도출하였으며,

* 가장 많은 용어가 연관된 네트워크는 **RSN32 (n = 38 terms)**,
* 어떠한 용어도 유의하게 연관되지 않은 네트워크는 **RSN01, RSN02, RSN26 (각각 n = 0)**이었습니다
  (그림 3, 표 1 참고).

해당 메타분석 맵(MAMs)이 각 RSN과 **유의하게 상관된 경우**,

* 평균 상관계수는 **r = 0.61**이었고,
* 최고 상관값은 **RSN14에서 r = 0.91**,
* 최저 상관값은 **RSN31에서 r = 0.32**로 나타났습니다 (그림 3).

각 네트워크에 대한 상세 결과는 보조자료(Supplementary Figures 7–39)에 수록되어 있습니다.

---

### 안정상태 네트워크의 인지 라벨 부여 (Resting-state network’s cognitive labeling)

#### 전문가 합의에 의한 인지 라벨링 (Consensus cognitive labeling)

각 네트워크에 대해 도출된 인지 용어를 기반으로, 6명의 전문가가 **표준화된 Cognitive Atlas 개념(Cognitive Atlas concepts)【37】**에 따라 합의하여 부여한 **인지 과정(cognitive processes)**은 \[표 2], \[그림 1], \[그림 2]에 제시되어 있습니다.

이들 라벨은 매우 다양한 범주의 인지 기능을 포괄합니다.
예를 들어, **감각 및 운동 기능(sensory and motor functions)**과 관련된 네트워크는 다음과 같습니다:

* **청각(auditory)**:

  * TN-01 (RSN14): **청각 지각(auditory perception)**

* **운동감각(somatomotor)**:

  * PcN-01 (RSN06): **사지 운동(movement of limb)**
  * PcN-02 (RSN04): **발성(articulation)**
  * PcN-03 (RSN11): **체성 감각(somatosensation)**
  * R-PcN (RSN25): **왼손 운동(movement of left hand)**
  * L-PcN (RSN21): **오른손 운동(movement of right hand)**

* **시각(visual)**:

  * ON-01 (RSN09): **시각 지각(visual perception)**
  * ON-02 (RSN29): **시각 형태 변별(visual form discrimination)**
  * ON-04 (RSN03): **운동 탐지 및 시각 객체 인식(motion detection, visual object recognition)**
  * OTN (RSN32): **객체 지각(object perception)**

또한, 우리는 **보다 통합적인 시각-운동 및 시공간적 처리(visuomotor and visuospatial processes)**와 관련된 RSN도 확인했습니다 (n = 3):

* D-FPN-01 (RSN10): **운동 계획(motor planning)**
* D-FPN-02 (RSN30): **운동 심상(motor imagery)**
* D-FPN-03 (RSN08): **공간 선택적 주의(spatial selective attention)**

---

우리는 또한 여러 **고차원 인지 과정(higher-level cognitive processes)**과 관련된 RSN들을 확인하였습니다 (n = 5):

* R-FTPN-02 (RSN20): **산술 계산(mental arithmetic)**
* L-InsFPN (RSN23): **음운 작업 기억(phonological working memory)**
* L-FTPN-02 (RSN12): **추론(reasoning)**
* mCingFPN (RSN16): **작업 기억(working memory)**
* FTPN-02 (RSN27): **읽기 및 산술(reading, mental arithmetic)**

기타 고차원 기능에는 다음과 같은 **인지 조절(cognitive control)**과 관련된 RSN이 포함됩니다 (n = 3):

* R-FInsN (RSN31): **인지 조절(cognitive control)**
* mCingInsN (RSN22): **수행 모니터링(performance monitoring)**
* FTPN-01 (RSN18): **기대(expectancy)**

또한, 다음과 같이 **의사결정(decision-making)**과 관련된 두 네트워크가 확인되었습니다 (n = 2):

* BGN (RSN24): **보상 예측(reward anticipation)**
* aCingN (RSN13): **의사결정(decision making)**

**언어(language)** 관련 용어들과 연결된 세 개의 네트워크는 다음과 같으며, 그 중 두 개는 명확히 좌반구에 편재되어 있습니다:

* L-FTN (RSN15): **구문 처리(syntactic processing)**
* L-FTPN-01 (RSN19): **문장 이해(sentence comprehension)**
* TN-02 (RSN33): **음성 지각(speech perception)** – 양측 측두이랑 포함

**사회적 인지(social cognition)**와 관련된 RSN도 두 개가 있었습니다 (n = 2):

* med-FN (RSN28): **마음 이론(theory of mind)**
* R-FTPN-01 (RSN17): **자기 모니터링 및 마음 이론(self-monitoring, theory of mind)**

다음 두 네트워크는 **디폴트 모드(default mode)**와 관련되어 있었으며,
메타분석 디코딩 결과에서 "default mode" 및 "default network" 용어와 유의하게 연관된 것으로 나타났습니다:

* med-TN (RSN05): **기억 회상(memory retrieval)**
* med-FPN (RSN07): **자기 지향적 처리(self-referential processing)**

한편, 메타분석 디코딩 절차에서 **어떠한 유의미한 연관성도 발견되지 않은** 네트워크는 3개였습니다 (n = 3):

* pCing-medPN (RSN01)
* R-FTPN-03 (RSN02)
* ON-03 (RSN26)

이들은 모두 **비유의적(n.s., non-significant)**으로 라벨링되었습니다.

---

### 잠재 의미 인지 라벨링 (Latent semantic cognitive labeling)

**완전히 데이터 기반(data-driven)**으로 수행된 **잠재 의미 분석(latent semantic analysis, LSA)** 기반 절차를 통해 얻어진 인지 라벨(cognitive labels)은 \[표 2]에 제시되어 있습니다.

전문가에 의해 수동으로 도출된 인지 라벨들과 비교했을 때,

* **LSA 기반 자동 라벨은 대체로 유사한 인지 영역(cognitive domains)**을 지칭하였습니다.

그러나 **주목할 만한 차이(notable exceptions)**도 일부 존재하였습니다. 예를 들어:

* **RSN07**은 전문가에 의해 **“자기 지향적 처리(self-referential processing)”**로 라벨링되었지만,
  LSA 라벨은 **“발산적 사고(divergent thinking)”**로 나타났습니다.

* **RSN29**는 전문가 라벨에서는 **“시각 형태 변별(visual form discrimination)”**이었으나,
  LSA에서는 **“과제 난이도(task difficulty)”**로 나타났습니다.

인지 영역(cognitive domains)의 일치는 대체로 유지되었으나,

* **세부 수준(level of specification)**에서는 차이를 보였습니다.
* 특히, LSA는 경우에 따라 **보다 구체적인 하위 과정(subprocess)**을 강조하는 경향이 있었습니다.

예를 들어:

* **RSN20**:

  * 전문가 라벨: **산술 계산(mental arithmetic)**
  * LSA 라벨: **공간 작업 기억(spatial working memory)**

* **RSN21**:

  * 전문가 라벨: **운동(movement)**
  * LSA 라벨: **운동 계획(motor planning)**

* **RSN28**:

  * 전문가 라벨: **마음 이론(theory of mind)**
  * LSA 라벨: **추론(inference)**

* **RSN33**:

  * 전문가 라벨: **음성 지각(speech perception)**
  * LSA 라벨: **청각적 문장 이해(auditory sentence comprehension)**

---

### 기본 모드 네트워크와 언어 네트워크에 대한 상세 결과

(Detailed results for default mode and language networks)

이 섹션에서는 본 연구 결과가 **기존 문헌(state of the art)**과 어떻게 부합하는지를 보여주는 대표적인 몇 가지 네트워크에 대해 중점적으로 설명합니다. 특히, **주요 구성 요소 분석(principal component analyses)** 결과가 어떻게 인지 라벨 합의의 근거로 사용되었는지를 보여줍니다. 각 RSN에 대한 모든 결과는 보조자료(supplementary materials)에 수록되어 있습니다.

---

#### 기본 모드 네트워크 (Default mode networks): RSN05, RSN07 — med-TN, med-FPN

두 개의 네트워크가 “default mode” 또는 “default network” 용어와 유의하게 디코딩된 것으로 나타났습니다:

* **RSN05 (med-TN)**
* **RSN07 (med-FPN)**
  → 관련 그림: \[그림 4]

**RSN05 (med-TN)**은 다음과 같은 영역을 포함합니다:

* 해마이랑(hippocampal gyri)
* 후대상회(posterior cingulum)
* precuneus
* 양측 각이랑(bilateral angular gyri)

“default mode” 관련 용어 외에도, **기억(memory)**과 관련된 용어들과 강하게 연관되었으며,
가장 높은 상관을 보인 세 용어는 다음과 같습니다:

* **자서전적 기억(autobiographical memory)**: r = 0.71, p < 0.001
* **일화 기억(episodic)**: r = 0.66, p < 0.001
* **자서전적(autobiographical)**: r = 0.64, p < 0.001
  → \[표 1], \[그림 4] 참조

이에 따라 RSN05에 대해 **전문가 합의 라벨은 "기억 회상(memory retrieval)"**으로 결정되었습니다 (\[표 2]).

---

**RSN07 (med-FPN)**은 다음과 같은 영역을 포함합니다:

* 내측 전전두 피질(medial prefrontal cortex, mPFC)
* 후대상피질(posterior cingulate cortex, PCC)
* precuneus
* 양측 각이랑(bilateral angular gyri)

이는 **기본 모드 네트워크(default mode network, DMN)**의 **정형적 해부학적 정의(canonical anatomical definition)**와 일치합니다.

이 네트워크는 총 **17개의 용어**와 유의한 디코딩 결과를 보였으며, 가장 높은 상관을 보인 두 용어는 다음과 같습니다:

* **default mode**: r = 0.84, p < 0.001
* **default network**: r = 0.72, p < 0.001
  → \[표 1], \[그림 4] 참조

RSN07의 **메타분석 활성화(meta-analytic activations)**를 기반으로 수행한 **주성분 분석(principal component analysis, PCA)**에서는

* **PC1**: 전체 용어들에 양의 가중치(positive loadings)를 보였으며, 상위 항목은 **내적 사고(internal thoughts)**와 관련된 것이었음

  * 예: 마음 이론(theory of mind), 정신화(mentalizing)
* **PC2**: 두 가지 유형의 사고를 대비시킴

  * **자기 중심적 사고(self-oriented thoughts)**: 자서전적 기억, 자기지향성, 개인적
  * **사회적 맥락의 사고(social-oriented thoughts)**: 믿음, 도덕, 사회

이에 따라 **전문가 합의 라벨은 “자기 지향적 처리(self-referential processing)”**로 결정되었습니다.

---

### 언어 네트워크 (Language networks): RSN15, RSN19, RSN33 — L-FTN, L-FTPN-01, TN-02

**언어 처리(language processing)**와 관련된 세 개의 네트워크는 다음과 같습니다:

* **L-FTN (RSN15)**
* **L-FTPN-01 (RSN19)**
* **TN-02 (RSN33)**

이 중 **L-FTN**과 **L-FTPN-01**은 좌반구에 편재된 네트워크이며,
**TN-02**는 **좌우 측두이랑(temporal gyri)** 전반에 걸쳐 확장되어 있습니다 (\[그림 5] 참조).

해부학적으로 세 네트워크는 모두 다음 영역에서 겹칩니다:

* **좌측 상측두구(sulcus of superior temporal sulcus, STS)**의 후방(posterior part)
* **상측두이랑(superior temporal gyrus)**
* **중측두이랑(middle temporal gyrus)**

이 외에도:

* **L-FTN**과 **L-FTPN-01**은 부분적으로 다음 영역에서 겹쳤습니다:

  * 하전두회(inferior frontal gyrus)
  * 중심전회(precentral sulcus)
  * 상전두회(superior frontal gyrus)
    단, **L-FTPN-01은 항상 L-FTN보다 전방(anterior)에 위치**했습니다.

* **L-FTPN-01**은 또한 다음 부위까지 더 확장됩니다:

  * 좌측 각이랑(angular gyrus)
  * 반면 L-FTN은 **두정엽 변연(supramarginal gyrus)**에서 끝났습니다.

---

**TN-02**와 유의하게 관련된 인지 용어들은 두 개의 **인지 주성분(cognitive principal components)**으로 그룹화되었습니다 (\[보조 그림 39]):

* **주성분 1 (PC1)** – 설명된 분산 56.5%:

  * **청각 양상(auditory modality)**과 관련된 용어들:

    * spoken, listening, speech, auditory, acoustic

* **주성분 2 (PC2)** – 설명된 분산 24.3%:

  * **언어 이해(language comprehension)** 관련 용어들과
    **비언어적 청각 정보(non-linguistic auditory information)** 용어 간의 대비:

    * 언어적: sentence comprehension, language network
    * 비언어적: communication, sounds, acoustic

공간적으로는:

* **좌측 STS 및 중측두 영역**에서 강한 양의 로딩(high positive loadings)
* **양측 상측두이랑과 우측 STS** 및 **우측 중측두이랑**에서 강한 음의 로딩(strong negative loadings)

이에 따라 **TN-02 (RSN33)**는 **"음성 지각(speech perception)"**이라는 Cognitive Atlas 기반 라벨이 부여되었습니다.

---

비록 **L-FTN**과 **L-FTPN-01**이 해부학적으로 일부 겹침에도 불구하고,
이 두 네트워크에 **연결된 인지 용어들의 집합(set of associated terms)**은 **상이**하였습니다.

---

#### L-FTN (RSN15)

* 전문가에 의해 부여된 라벨: **구문 처리(syntactic processing)**
* 이 네트워크에 대한 주성분 분석(PCA) 결과,

  * **단일 주성분(single unitary component)**이 전체 분산의 **90.7%**를 설명함
  * 주요 연관 용어들:

    * **동사(verbs)**
    * **구문(syntactic)**
    * **문장 이해(sentence comprehension)**
      → 보조 그림 21 참조

---

#### L-FTPN-01 (RSN19)

* 전문가에 의해 부여된 라벨: **문장 이해(sentence comprehension)**
* PCA 결과, 두 개의 주성분이 확인됨:

  * **주성분 1 (56.4% 분산 설명)**:

    * **언어 이해의 언어학적 측면(linguistic aspects of language comprehension)**과 관련된 용어들:

      * language comprehension, sentence comprehension, syntactic, semantic

  * **주성분 2 (12.3% 분산 설명)**:

    * **의미 표현(semantic representation)**과 관련된 고차원 인지 용어들:

      * mentalizing, theory of mind, inference

공간적으로는:

* **주성분 1**은 다음 영역에서 강하게 표현됨:

  * 좌측 상측두구(left STS)
  * 전측 하전두이랑(anterior inferior frontal gyrus)

* **주성분 2**는 다음 영역에서 표현됨:

  * 좌측 각이랑(angular gyrus)
  * 측두극(temporal pole)
  * 전내측 전두이랑(anterior medial frontal gyrus)
    → 보조 그림 25 참조

---

## 논의 (Discussion)

**안정상태 네트워크(resting-state networks, RSNs)**의 **인지적 관련성(cognitive relevance)**은 아직 명확히 이해되지 않았습니다. 이 문제를 해결하기 위해, 우리는 **Groupe d’Imagerie Neurofonctionnelle Network Atlas (GINNA)**를 제안합니다. 이는 **1812명의 안정상태 fMRI 데이터**를 바탕으로 구축된 **포괄적인 RSN 아틀라스**이며, 인간 뇌를 **33개의 개별 네트워크**로 나누어 **인지적 특성(cognitive characterization)**을 제공하는 자료입니다.

우리는 GINNA 네트워크들과 **Neurosynth 데이터베이스【25】로부터 추출된 메타분석 맵(meta-analytic maps)** 간의 **형태학적 유사성(topographical similarities)**을 체계적으로 분석하였습니다. 이 과정에서 사용된 기법은 **단순한 Pearson 상관계수 기반의 공간 유사도 측정(spatial similarity using Pearson correlation)**이었지만,

* 그럼에도 불구하고, **RSN에 관련된 인지 과정을 탐색하는 데 매우 유용**한 방식임을 본 연구는 보여줍니다.

우리는 GINNA RSNs와 관련된 **인지 용어(cognitive terms)**를 **정량적 메타분석 디코딩(quantitative meta-analytic decoding)**을 통해 도출함으로써, RSN의 **경험적 인지 특성화(empirically informed cognitive characterization)**를 제공합니다.

---

**과제 기반 메타분석 맵(task-derived meta-analytic maps)**과 RSN을 비교하는 접근은 특히 유효한데,
이는 **RSN이 인지 기능의 가능한 구성요소(possible repertoire of cognitive functions)**를 **잠재적으로 탐색(prospective exploration)**하는 역할을 하기 때문입니다【38】.

또한 **다변량 패턴 분석(multivariate pattern analysis)** 문맥에서, Neurosynth 기반 디코딩은

* 더 복잡한 디코더들과 **유사한 성능**을 보이며【39】,
* 짧은 과제 기반 fMRI 블록에서도 참가자의 **인지 영역(cognitive domains)**을 성공적으로 디코딩할 수 있음이 입증되었습니다【29】.

따라서 비록 단순하고 계산 비용이 낮은 방식이지만,
**활성화 맵과의 형태 유사성 기반 디코딩은 이론적으로 정당화될 수 있는 접근**입니다.

---

지금까지 존재하는 **기존 뇌 네트워크 분할(parcellation)** 방식들 중 일부는 **인지 라벨(cognitive labeling)**을 제공하지만,
대표적으로 **Yeo et al. (2011)【15】**는 과제 기반 네트워크와의 **시각적 유사성(visual similarity)**만을 기준으로 기능을 연결 지었으며,
이는 RSN을 **정확하게 식별하는 데 실패하는 경우가 많음**이 입증되었습니다【12】.

또한, 일부에서는 네트워크를 **해부학적 프로파일(anatomical profile)**을 기준으로 명명할 것을 제안하기도 하였습니다【11】.

이에 비해 GINNA는:

* 각 RSN에 대해 **해부학적으로 기반한 명명(anatomically grounded taxonomy)**을 제공하면서,
* 동시에 **인지적 과정(cognitive processes)**도 함께 제시함으로써,
* 이 두 가지 관점을 **조화롭게 통합(reconcile)**합니다.

---

기존의 RSN 인지 특성화 시도들은 대부분:

1. **과제 기반 네트워크(task-based networks)**와의 **형태적 유사성(topographical similarity)**에 의존하거나【23】
2. **BrainMap【24】로부터 도출된 광범위한 인지 영역(broad cognitive domains)**을 기반으로 하였습니다.

이에 비해, 본 연구는 **정밀한 단일 인지 용어(single cognitive term precision)**를 지원하는 **Neurosynth**를 사용하여,
**안정상태에서 도출된 네트워크**에 대한 **경험적이고 고해상도의 인지 특성화(high-resolution cognitive characterization)**를 가능하게 했다는 점에서 큰 차별점을 가집니다.

---

**안정상태 네트워크(RSNs)**의 인지적 특성화를 **구체적 인지 과정(specific cognitive processes)**과 연결 짓는 작업은, **인지신경과학(cognitive neuroscience)** 분야에 있어 반드시 필요한 과업입니다. 그 이유는 다음과 같습니다:

1. **심리학적으로 잘 정의된 개념들(psychological constructs)**을 참조함으로써,
   각 RSN에 대해 **경험적 예측(empirical predictions)**을 수행할 수 있게 됩니다.
   → 이는 “시각(visual)”이나 “조절(control)”과 같은 **모호한 범주적 용어(broad domains)**보다 훨씬 더 유용합니다.

2. RSN의 기능에 대한 해석이 **신경영상 문헌(neuroimaging literature)**과의 비교를 통해 이루어질 수 있기 때문에,
   본 연구에서의 인지적 특성화는 다음 두 가지 측면의 현재 지식을 요약하려는 시도입니다:

   * (1) **인지 개념의 개념화(conceptualization of cognitive concepts)**:
     → 이는 연구들에 나타난 용어들의 분포와, Neurosynth가 이를 어떻게 추출하는지에 반영됩니다.

   * (2) **이러한 개념들의 뇌 내 기반(brain underpinnings)**:
     → 이는 메타분석 맵(meta-analytic maps)의 **형태(topology)**를 통해 나타납니다.

따라서 뇌에서 인지가 어떻게 조직되는지를 이해하려는 목적이라면,
RSN이 수행하는 **가설적 인지 과정(putative processes)**을 단순히 “시각”이나 “변연계”처럼 넓고 모호한 용어로 표현하기보다는,
**마음 이론(theory of mind)**, **시각 지각(visual perception)**과 같은 **인지 이론에서 사용되는 구체 용어들(specific theoretical terms)**로 표현하는 것이 훨씬 바람직합니다.

게다가 본 연구에서 부여된 거의 모든 인지 과정 라벨은 **Cognitive Atlas Ontology**에 수록된 개념에 해당하며,
(단, “자기 지향적 처리(self-referential processing)”는 예외)
→ 이는 연구자들이 각 용어의 **정의(definition)**를 명확히 참조함으로써 **개념적 모호성(disambiguation)**을 줄이고,
→ **공통된 해석의 틀(common ground)**을 마련할 수 있도록 해줍니다.

🔗 Cognitive Atlas의 개념 정의는 보조자료 및 다음 링크에서 확인할 수 있습니다:
[https://www.cognitiveatlas.org/concepts/categories/all](https://www.cognitiveatlas.org/concepts/categories/all)

---

GINNA 아틀라스는 기존 아틀라스들과 **세분화도(granularity)**에서 뚜렷한 차이를 보입니다.

이러한 **더 높은 수준의 세분화(finer granularity)**는 일반적으로 간과되어 왔으나,
실제로는 **유용한 분석 단위(beneficial units of analysis)**가 될 수 있다는 점이 점차 밝혀지고 있습니다.

예를 들어, 심리학에서 도출된 다양한 **네트워크 개념(network constructs)** —
예: “공포 네트워크(fear network)”, “작업 기억 네트워크(working memory network)” 등 —
이들을 상위 수준의 **대규모 네트워크(large-scale networks)**로 그룹화할 경우,

* 서로 전혀 다른 **인지 과정(cognitive processes)**들이 한데 묶여
* **기능적으로 이질적인 결과(functional heterogeneity)**를 야기할 수 있음이 입증되어 왔습니다【16】.

또한, 뇌 회로(brain circuits)의 **기능적 좌우 분할(functional lateralization)**은

* 인간 뇌의 **핵심 조직 원리(core organizational principle)**임에도 불구하고,
* 대부분의 기존 아틀라스는 이를 반영하지 않고
* **양반구 대칭 네트워크(bilateral networks)**만을 제시합니다.

이에 반해 GINNA에서는:

* 여전히 일부 양반구 네트워크가 존재하지만,
* **더 높은 세분화도로 인해** 기존 양측성 네트워크들이
  **각 반구의 동형 영역(homotopic counterparts)**으로 **분절(fragmentation)**되는 경우도 관찰되었습니다.

예를 들어:

* **손 운동 체감계통(hand somatomotor system)**은

  * **왼손과 오른손 운동성(somatomotor homunculus)**을 각각 반영하는
  * **두 개의 동형 네트워크(homotopical systems)**로 나뉘었습니다.

또 다른 예는:

* **전두-측두-두정 네트워크(fronto-temporo-parietal networks)**로,

  * 좌반구의 **L-FTPN01**은 **문장 이해(sentence comprehension)**,
  * 우반구의 **R-FTPN01**은 **자기 모니터링 및 마음 이론(self-monitoring and theory of mind)**에 관련된 것으로 나타났습니다.

이러한 **편측화된 RSN(lateralized RSNs)**의 식별은
→ GINNA가 기능적으로 **의미 있는 단위(functionally relevant units)**를 제공한다는 것을 시사합니다.

---

본 연구는 GINNA 아틀라스를 통해, **기존 대규모 네트워크들(large-scale networks)**이
여러 개의 보다 **세분화된 RSN들(finer-grained RSNs)**로 나뉠 수 있음을 보여주었습니다.
이들 각각은 **구별되는 인지 특성(distinct cognitive profiles)**을 가지고 있습니다.

예를 들어, 전통적으로 단일한 "시각 네트워크(visual network)"로 간주되던 영역은
GINNA에서는 다음과 같이 분할됩니다:

* **ON-01 (RSN09)**: **시각 지각(visual perception)**
* **ON-02 (RSN29)**: **시각 형태 변별(visual form discrimination)**
* **ON-04 (RSN03)**: **운동 탐지 및 시각 객체 인식(motion detection and object recognition)**
* **OTN (RSN32)**: **객체 지각(object perception)**

이들 시각 네트워크 각각은, **해부학적·기능적 관점**에서 볼 때 명확히 구분되는 하위 영역에 해당합니다.
→ 이는 기존 시각 시스템에 대한 인지 신경과학 문헌과 일치합니다.

또한, 전통적으로 **하나의 디폴트 모드 네트워크(DMN)**로 간주되어 온 영역 역시

* **RSN05 (med-TN)**: **기억 회상(memory retrieval)**
* **RSN07 (med-FPN)**: **자기 지향적 처리(self-referential processing)**
  와 같이 두 개의 기능적으로 뚜렷한 구성 요소로 분리되었습니다.

또 다른 예로, 일반적으로 **단일 언어 네트워크(language network)**로 다뤄지던 영역은 GINNA에서는

* **L-FTN (RSN15)**: **구문 처리(syntactic processing)**
* **L-FTPN-01 (RSN19)**: **문장 이해(sentence comprehension)**
* **TN-02 (RSN33)**: **음성 지각(speech perception)**
  로 세분화되었습니다.

이처럼 GINNA는 **해부학적·기능적 차원 모두에서 더 높은 해상도**를 제공하며,
이를 통해 **기존 네트워크 정의 방식의 제한점**을 보완할 수 있습니다.

---

### 한계점 및 향후 방향 (Limitations and future directions)

본 연구는 다음과 같은 **몇 가지 주요 한계점(limitations)**을 가집니다.

---

1. **RSN 추출을 위해 단일 클러스터링 알고리즘(single clustering algorithm)**만 사용하였고,
   → **개별 참가자의 안정상태 데이터(individual-level resting-state data)**가 아니라,
   → **그룹 수준의 데이터(group-level data)**에서 도출된 신호를 기반으로 하였습니다.

이는 기능적 연결망 분석에서 자주 사용되는 전략이지만,

* **참가자 간 이질성(inter-subject heterogeneity)**을 포착하지 못할 수 있으며,
* **더 미세하거나 개별화된 네트워크(subtler or idiosyncratic networks)**는 놓칠 수 있습니다.

최근에는 개인 수준에서의 신경망 정밀 분석을 강조하는 경향이 강해지고 있으며【40】,
→ 추후 연구에서는 이러한 방식이 **GINNA 아틀라스의 세분화도(granularity)**를 더욱 향상시킬 수 있을 것입니다.

---

2. 본 연구에서 사용한 **형태 기반 메타분석 디코딩(Neurosynth decoding)**은,

   * 공간적으로 활성화된 패턴과의 **단순 유사도 측정(spatial similarity)**에 기초하고 있으며,
   * **통계적 인과성(statistical causality)**이나 **기능적 메커니즘(functional mechanisms)**을 제공하지 않습니다.

따라서 특정 RSN과 인지 용어 간의 연관은,

* 반드시 **기능적 가설(functional hypotheses)**로 이어져야 하며,
* 이러한 가설은 **독립적인 실험적 연구**를 통해 **검증될 필요가 있습니다.**

---

3. 또한 GINNA는 **기초 인지 과정(basic cognitive processes)**에 대해서만 초점을 맞췄으며,

* **정서(emotion)**, **동기(motivation)**, **통증(pain)**, **신체 항상성(homeostasis)** 등
* 보다 복합적인 **체계 수준의 기능(system-level functions)**은 다루지 않았습니다.

이는 부분적으로 **Neurosynth 데이터베이스의 제약**에서 비롯된 것입니다.

앞으로의 확장은:

* **다양한 감정, 정동, 사회 정체성(social identity), 도덕성, 사회적 상호작용** 등의
  고차원 개념들을 포함한 **새로운 용어 집합(extended vocabulary)** 구축을 통해 이루어져야 할 것입니다.

---

4. 마지막으로, 본 연구는 **성인 뇌(adult brain)**만을 기반으로 하고 있으며,

* **발달 단계(developmental stages)**, **노화(aging)**, **정신·신경 질환(neuropsychiatric conditions)**에서의
  RSN 특성 변화에 대한 고려는 포함하지 않았습니다.

→ GINNA 아틀라스의 확장 버전은

* 이러한 다양한 인구 집단(subpopulations)에 대한 **별도의 인지 특성화**를 제공할 수 있으며,
* 향후 **병태생리 연구(pathophysiology)**나 **발달 신경과학(developmental neuroscience)** 분야에 응용될 수 있습니다.

---

## 결론 (Conclusion)

본 연구는, **대규모 안정상태 기능 연결망 분석(large-scale resting-state functional connectivity analysis)**과
**인지 신경영상 메타분석(cognitive neuroimaging meta-analysis)**을 통합함으로써,
새로운 뇌 네트워크 아틀라스인 **GINNA (Groupe d’Imagerie Neurofonctionnelle Network Atlas)**를 제시합니다.

GINNA는 다음과 같은 특징을 갖습니다:

* **정량적 인지 라벨링(quantitative cognitive labeling)**이 부여된
* **33개의 안정상태 네트워크(resting-state networks, RSNs)**로 구성되어 있으며
* 각 네트워크는 **기능적으로 해석 가능한 단위(functionally interpretable units)**로 정의됩니다.

본 아틀라스는 다음과 같은 방식으로 활용될 수 있습니다:

1. **실험 연구의 뇌 활성 결과(brain activation findings)**를,

   * 기존의 단순 해부학적 영역(atlas-based anatomical regions)뿐만 아니라,
   * **기능적으로 정의된 RSNs**에 기반하여 해석할 수 있도록 도와줍니다.

2. **인지 기능과 뇌 연결성 간의 관계**에 대한

   * 새로운 가설(hypotheses) 제시 및
   * **기계학습 기반 디코더(machine-learning decoders)** 설계 등
   * 후속 연구를 위한 출발점이 될 수 있습니다.

3. 향후에는 GINNA를 기반으로 한

   * **개별 맞춤형 뇌 네트워크 분석(individualized network-based analyses)**,
   * **질환 모델링(disease modeling)**,
   * **정신과적 진단 보조(cognitive phenotyping for psychiatry)** 등의
     응용 가능성도 존재합니다.

GINNA는 공개된 데이터와 재현 가능한 방법론을 기반으로 구축되었으며,
→ [https://ginna.sub.univ-amu.fr](https://ginna.sub.univ-amu.fr)에서 무료로 사용할 수 있습니다.

이를 통해 연구자들은 자신의 fMRI 결과를 **인지적으로 해석 가능한 RSN 레퍼런스(reference)**에 기반하여 비교하고,
**기능적 의미(functional meaning)**를 보다 깊이 있게 파악할 수 있을 것입니다.
