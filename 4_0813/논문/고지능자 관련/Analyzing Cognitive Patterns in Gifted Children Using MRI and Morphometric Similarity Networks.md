**"Analyzing Cognitive Patterns in Gifted Children Using MRI and Morphometric Similarity Networks"**

---

### 초록 (Abstract)

비침습적 신경영상(neuroimaging)의 발전, 특히 **구조적 자기공명영상(structural magnetic resonance imaging, sMRI)** 기술의 발전은 **구조적 뇌 네트워크(structural brain networks, SBNs)**의 구축을 가능하게 하여, 해부학적 연결(anatomical connections)을 생체 내(in vivo)에서 매핑(mapping)할 수 있게 되었다. 본 연구는 sMRI 데이터로부터 생성된 **개인별 형태측정 유사성 네트워크(individual morphometric similarity networks, MSNs)**를 통해, 아동의 지능 수준 차이에 따른 뇌 네트워크 구조의 차이를 조사한다.

집단 수준(group-level)과 개인 수준(individual-level) 분석을 통해, 본 연구는 인지 수행(cognitive performance)과 관련된 주요 **위상적 특성(topological features)**을 규명하고, SBN 분석에 적합한 **연결 밀도(connection density)**를 제시하고자 한다. 연결 밀도는 전역 및 노드 수준의 위상적 특성에 강한 영향을 미치며, 안정적이고 최적의 결과를 위해 p = 0.05에서 0.15 범위를 권장한다.

영재(gifted) 집단은 다음과 같은 특성을 보였다:

* **반구 내 연결성(intra-hemispheric connectivity)** 및 **모듈 내 연결성(intra-modular connectivity)**이 더 강함
* 좌우 반구 내 연결의 분포가 더 균형적임
* 평균 **다기능성(mean versatility)**이 낮음

이러한 특성은 효율적이고 안정적인 인지 처리(efficient and stable cognitive processing)를 지지한다.

또한, **von Economo 기반 해부학적 모듈성(anatomical modularity)** 분석 결과에 따르면, 높은 인지 수행은 특정 영역(예: **이차 감각 영역(secondary sensory area)**, **운동-연합 영역(motor to association area)**, **이차 감각-변연계 영역(secondary sensory to limbic area)**)에서의 연결성이 증가하고, 특정 모듈 연결(예: **운동-섬엽 영역(motor to insular area)**, **연합-이차 감각 영역(association to secondary sensory area)**, **운동-이차 감각 영역(motor to secondary sensory area)**)에서는 선택적인 감소가 나타났다.

더불어, **참여 계수(participation coefficient)**, **국소 효율성(local efficiency)** 등의 위상적 특성이 인지 수행과 연관되어 있음이 드러났다.

이러한 발견은 아동의 인지 수준과 관련된 SBN의 구조에 대한 중요한 통찰을 제공한다.

---

## 1 서론 (INTRODUCTION)

인지 능력(cognitive abilities)의 신경학적 기반(neural basis)을 이해하는 것은 오랫동안 인지신경과학(cognitive neuroscience)의 핵심 목표였다. 그동안 상당한 진전이 있었음에도 불구하고, 특히 **영재(gifted individuals)**의 뇌에서의 구조적 및 기능적 차이를 이해하는 데에는 여전히 중요한 공백이 존재한다.

이러한 공백을 메우기 위한 유망한 접근법 중 하나는 **뇌 네트워크(brain networks)** 연구로, 이는 서로 다른 뇌 영역들 간의 연결성(connectivity)과 상호작용(interactions)을 탐구한다. 최근의 **비침습적 신경영상기술(non-invasive neuroimaging techniques)**의 발전—특히 **구조적 자기공명영상(structural magnetic resonance imaging, sMRI)** 및 **확산 MRI(diffusion MRI)**—은 해부학적 연결(anatomical connections)을 생체 내에서 매핑할 수 있게 해주었다(Genon et al., 2022; Lo et al., 2011). 이러한 기술들은 뇌를 **노드(nodes, 뇌 영역)**와 **엣지(edges, 영역 간 연결)**로 구성된 그래프(graph)로 모델링하여 **구조적 뇌 네트워크(structural brain networks, SBNs)**를 구성할 수 있게 하였으며, 이로써 그래프 이론(graph theory)을 활용하여 뇌의 조직 구조와 그것의 인지 능력과의 관계를 탐색할 수 있는 기초를 마련하였다(Faskowitz et al., 2022).

SBN을 구성하는 주요 접근법은 다음 두 가지이다:

1. **확산가중영상(diffusion-weighted imaging, DWI)** 기반의 **트랙토그래피(tractography)**
2. **sMRI 기반 구조 공분산 네트워크(structural covariance networks, SCNs)**

SCN은 전통적으로 **피질 두께(cortical thickness)** 같은 단일 형태측정 지표의 공분산을 다수 피험자 집단 간(region 간 across subjects)에서 계산하는 방식이다(Solé-Casals et al., 2019). 이 방법은 집단 수준에서의 뇌 조직 구조를 이해하는 데에 큰 기여를 해왔지만, 최근에는 **개인 수준의 SCN(individual-level SCN)**이 도입되어, 여러 형태측정(feature)들을 통합함으로써 보다 정밀하고 개인화된 뇌 구조 분석이 가능해졌다(Kong et al., 2015; Li et al., 2017; Yu et al., 2018; Seidlitz et al., 2018; Li et al., 2021; Sebenius et al., 2023; Sun et al., 2024a,b).

이 분야의 주목할 만한 발전 중 하나는 **형태측정 유사성 네트워크(morphometric similarity network, MSN)**이다(Seidlitz et al., 2018). MSN은 sMRI에서 유도된 여러 구조적 특징을 이용해 개인별 뇌 네트워크를 구축하며, 뇌 영역 간 형태측정 특성 벡터 간의 쌍별 상관관계(pairwise correlations)를 기반으로 한다. 이 방법은 뇌의 구조적 조직(structural organization)을 보다 정밀하게 조사할 수 있으며, 생물학적으로 의미 있는 패턴을 밝혀내는 데에 유용하다는 점이 입증되었다.

기존 연구들에서는 성별(Sun et al., 2015), 인지 능력(Park and Friston, 2013), 그리고 신경퇴행성 질환(neurodegenerative diseases)의 진행(Sun et al., 2024b) 등 다양한 생물학적 특성과 관련된 SBN 패턴을 밝혀낸 바 있다. 그러나 여전히 다음과 같은 중요한 질문들이 미해결 상태이다:

* MSN의 **위상적 특성(topological properties)**은 인지 수행(cognitive performance)과 어떤 관계가 있는가, 특히 **아동**에서는 어떠한가?
* **모듈 구조(modular structure)** 및 **반구 전문화(hemispheric specialization)**는 영재의 **신경 효율성(neural efficiency)**에 어떻게 기여하는가?
* 다양한 **연결 밀도(connection densities)**는 뇌 네트워크의 특성에 어떤 영향을 미치는가?

이러한 질문들은 인지 능력의 구조적 기반을 이해하는 데에 핵심적인 질문들이다.

본 연구는 이러한 공백을 메우고자 **sMRI 데이터로부터 MSN을 구축하고**, **영재(gifted)** 및 **일반 아동(control group)** 간의 인지 수행과 뇌 네트워크 위상 구조의 관계를 분석하였다. 특히, 본 연구는 다음과 같은 분석을 수행하였다:

* **von Economo (VE)**에 기반한 **모듈 연결(modular connections)** 비교
* 다양한 **연결 밀도(connection densities)**의 영향 분석
* VE 기반 **모듈 내/간 연결(intra-/inter-modular connections)** 분석
* **반구 내/간 연결(intra-/inter-hemispheric connections)** 분석
* **노드 및 전역 위상 특성(nodal and global topological features)**과 인지 수행 간의 관계 분석
* 특정 VE-Region 간 연결과 인지 수행의 관련성 분석

이러한 **집단 수준(group-level)** 및 **개인 수준(individual-level)** 분석의 결합을 통해, 본 연구는 **영재성(giftedness)**의 신경 메커니즘(neural mechanisms)에 대한 새로운 통찰을 제공하며, **해부학적 모듈성(anatomical modularity)**, **반구 전문화(hemispheric specialization)**, 그리고 **위상 특성(topological features)**이 **효율적인 인지 처리(efficient cognitive processing)**에 어떻게 기여하는지를 강조한다.

논문의 구조는 다음과 같다:

* **2장**: 사용된 데이터셋과 분석 방법(methods)
* **3장**: 분석 결과
* **4장**: 결과 해석 및 논의
* **5장**: 결론

---

## 2 자료 및 방법 (MATERIALS AND METHODS)

### 2.1 데이터 (Data)

#### 2.1.1 참가자 (Participants)

본 연구에서는 **정상 발달 남아** 29명의 **sMRI** 및 **인지 검사(cognitive tests)** 데이터를 사용하였다. 참가자들은 모두 오른손잡이(right-handed)이며, 정신적 또는 신경학적 장애 이력이 없다(Solé-Casals et al., 2019). 원시(익명화된) MRI 데이터 및 피질 두께(cortical thickness) 데이터는 OpenNeuro 저장소에서 접근 가능하다:
[https://openneuro.org/datasets/ds001988](https://openneuro.org/datasets/ds001988)

참가자는 다음 두 그룹으로 분류된다:

* **일반 그룹(control group, CG)**: 14명
* **영재 그룹(gifted group, GG)**: 15명

참가자 정보는 **표 1**에 제시되어 있으며, 두 그룹 간 **연령 차이는 통계적으로 유의하지 않지만**, **전체 IQ(full-scale IQ)**에서는 **유의한 차이**가 나타난다.

**표 1: 참가자 정보**

| 그룹 | CG (평균±표준편차) | GG (평균±표준편차) |
| -- | ------------ | ------------ |
| 연령 | 12.53±0.77   | 12.03±0.54   |
| IQ | 122.71±3.89  | 148.80±2.93  |

---

#### 2.1.2 구조적 MRI 데이터 (sMRI Data)

MRI 촬영은 3T 스캐너에서 수행되었으며, 고해상도 T1 강조 이미지(T1-weighted images)가 **MPRAGE 3D 프로토콜**을 통해 얻어졌다. 본 연구에서는 이전 연구(Solé-Casals et al., 2019)에서 제안된 sMRI 전처리 방법을 채택하였다.

전처리는 **FreeSurfer v5.3**를 사용하였으며, 이 소프트웨어는 영상의 밝기(intensity) 및 연속성 정보에 기반하여 **3차원 피질 표면 모델(3D cortical surface model)**로부터 **피질 두께(cortical thickness)**를 추정한다(Fischl and Dale, 2000). 피질 재구성 결과는 두 명의 숙련된 연구자가 독립적으로 검토하여 품질 기준을 충족하는지 확인하였다.

각 피험자의 뇌는 **FreeSurfer의 표준 템플릿(fsaverage)**을 기반으로 약 **500 mm² 크기**의 영역 308개(**R = 308**)로 나뉘었으며, 이 때 **Desikan-Killiany atlas(Desikan et al., 2006)**에 정의된 영역을 세분화하는 **backtracking 알고리즘**이 사용되었다. 각 피험자의 고유한 MPRAGE 영상으로의 등록은 **mri\_surf2surf** 명령어를 통해 **비선형(surface-based) 정합(non-linear registration)**으로 수행되었다(Ghosh et al., 2010).

이렇게 분할된 **308개 영역**은 **von Economo (VE)**의 **세포구조학적 피질 분류(cytoarchitectonic cortical types)**에 따라 **7개의 구조적 유형(structural types)**으로 분류된다. 요약하면 다음과 같다:

* **Type 1**: 층상 구조(laminar differentiation)가 거의 없는 영역 → 주로 **운동 피질(primary motor cortex)** 및 **전중심 회(precentral gyrus)**
* **Type 2 & Type 3**: 일반적으로 **연합 피질(association cortices)** 포함
* **Type 4 & Type 5**: 각각 **이차 감각 영역(secondary sensory areas)** 및 **일차 감각 영역(primary sensory areas)**에 해당

von Economo의 원래 분류는 **6층 대뇌겉질(isocortex)**과 **중간겉질(mesocortex)**, **원시겉질(allocortex)**을 구분하지 않기 때문에, 본 연구에서는 다음 두 가지 **추가 하위 유형(subtypes)**을 도입하였다:

* **Type 6 (변연계 피질, limbic cortex)**: 내후각피질(entorhinal cortex), 전소엽피질(presubiculum), 후대상피질(retrosplenial cortex), 대상회(cingulate cortex) 포함 → 주로 **원시겉질(allocortex)**에 속함
* **Type 7 (섬엽 피질, insular cortex)**: 무과립(agranular), 미과립(dysgranular), 과립(granular) 영역 포함

이러한 구조적 분류는 이전 연구들(Solé-Casals et al., 2019; Seidlitz et al., 2018; Vása et al., 2018; Vértes et al., 2016)을 바탕으로 하며, 본 연구에서는 **VE 기반 영역(VE-Regions)**을 중심으로 **해부학적 모듈성 분석(anatomical modularity analysis)**을 수행한다.

---

## 2.2 방법 (Methods)

본 연구에서는 sMRI 데이터로부터 **형태측정 유사성 네트워크(Morphometric Similarity Networks, MSNs)**를 구축하였다. **집단 수준 분석(group-level analyses)**은 일반 그룹(CG)과 영재 그룹(GG)의 평균 MSN을 비교하여 뇌 네트워크의 위상 구조에서 나타나는 주요 차이를 식별하는 데 목적이 있다. 또한 **개인 수준 분석(individual-level analyses)**을 통해 인지 수행(cognitive performance)과 뇌 네트워크 구조 간의 관계를 탐색하였다.

---

### 2.2.1 네트워크 구축 (Network Construction)

각 피험자마다 **형태측정 유사성 네트워크(MSN)**를 구축하였다. 이는 각 **뇌 영역(brain region)** 간의 **구조적 연결성(structural connectivity)**을 나타낸다(Seidlitz et al., 2018).

MSN은 개별 피험자의 다중 모달 MRI 특성 세트를 기반으로, 각 뇌 영역 간의 **형태측정 특성 벡터(morphometric feature vector)** 사이의 **쌍별 상관계수(pairwise correlation)**를 계산하여 **형태측정 유사성 행렬(morphometric similarity matrix)**을 생성한다.

이 연구에서는 **T1 강조 영상(T1-weighted MRI)**에서 추출한 총 **5가지 형태측정 특성(morphometric features)**을 사용하였다. 각 샘플마다 $308 \times 5$ 크기의 특성 행렬을 갖는다:

* **총 표면적(total surface area, tSA)**
* **총 회색질 부피(total gray matter volume, tGMV)**
* **평균 피질 두께(average cortical thickness, aCT)**
* **적분 절댓값 평균 곡률(integrated rectified mean curvature, iMC)**
* **적분 절댓값 가우시안 곡률(integrated rectified Gaussian curvature, iGC)**

이 5가지 특성만으로 구축한 MSN이 더 많은 특성을 사용할 때와 유사한 결과를 보인다는 점이 입증되었으며, 특히 tSA, tGMV, aCT, iGC는 **가장 변별력이 높은(discriminative)** 특성으로 확인되었다(Seidlitz et al., 2018; Zhang et al., 2021).

각 특성 벡터는 z-점수(z-score)로 정규화된 후 상관계수 계산에 사용된다. MSN에서 노드는 Desikan-Killiany atlas 기반으로 정의된 308개 뇌 영역이며, 엣지는 두 영역 간의 정규화된 특성 벡터 간의 **피어슨 상관계수(Pearson’s correlation coefficient, PCC)**이다.

* PCC 값이 1에 가까울수록 두 영역이 유사하다는 뜻이며,
* -1에 가까울수록 반상관(anticorrelation)을 의미한다.
* 대각선 항목은 자기 자신과의 상관이므로 1이지만, **MSN 행렬의 대각선은 모두 NaN으로 설정**하였다.

---

### 2.2.2 MSN의 집단 비교 분석 (Group Comparison Analyses for MSNs)

**그림 1**에 나타낸 것처럼, 각 그룹(CG, GG)의 평균 뇌 네트워크를 계산하여 비교 분석을 수행하였다. 분석 내용은 다음과 같다:

---

#### • VE-Region 기반 연결 분석 (VE-Region analysis for group brain networks)

먼저 MSN의 행렬을 **7개의 VE-Region** 기준으로 재정렬한다. 각 네트워크 A에서 **VE-Region k와 l 사이의 연결**은 다음과 같이 정의된다:

$$
A_{kl} = A_{ij} \quad (i \in N_k, j \in N_l, i \ne j)
$$

여기서

* $A_{kl}$은 VE-Region k와 l 사이의 모든 연결을 포함한 서브 행렬,
* $N_k, N_l$은 각각 VE-Region k, l에 속하는 노드들의 집합
* $k = l$일 경우는 **intra-VE 연결**,
* $k \ne l$일 경우는 **inter-VE 연결**

**평균 VE 연결 강도(mean VE connection strength)** $E(k, l)$는 다음과 같이 정의된다:

$$
E(k, l) = \frac{1}{n_{kl}} \sum A_{kl}
$$

* $n_{kl}$: 두 VE-Region 사이의 총 연결 수

**집단 간 유의한 차이 분석**은 **Mann–Whitney U 검정**을 통해 수행되며, 다음과 같이 표현된다:

$$
[P_{kl}, zval_{kl}] = U[\text{vec}(A_{kl}^G), \text{vec}(A_{kl}^C)]
$$

* $A_{kl}^G, A_{kl}^C$: 각각 GG, CG의 VE-Region 간 연결
* 벡터 형태로 변환 후 검정 수행
* $P_{kl} \leq 0.05$: 통계적으로 유의한 차이
* $zval_{kl} \geq 1.96$: 유의수준 0.05에 해당하는 정규 분포 통계값

주의: MSN에는 음의 값이 존재하므로 zval 해석은 제한됨.

---

#### • 연결 밀도에 따른 분석 (Analysis across different density)

모든 네트워크를 **MST(Minimum Spanning Tree)** 기반으로 생성하여 연결이 보장되도록 한다(Van Wijk et al., 2010).

* MST는 R개의 노드를 정확히 R−1개의 엣지로 연결하는 최소 연결 서브그래프
* 이후 엣지를 추가하여 목표 **연결 밀도(connection density)**를 맞춘다

네트워크의 연결 밀도 p는 전체 가능한 엣지 수 대비 실제 엣지 수의 비율:

$$
\text{Density } p = \frac{\text{엣지 수}}{\frac{R(R-1)}{2}} \quad \text{(R=308)}
$$

사용된 p 값 목록:

$$
\{0.0065, 0.01, 0.05, 0.1, ..., 1.0\}
$$

CG 및 GG 그룹의 MST 네트워크에서 비제로 항목들을 추출하여 각각 $t^C_p$, $t^G_p$로 정의한 후, Mann–Whitney U 검정:

$$
[P_p, zval_p] = U(t^G_p, t^C_p)
$$

---

#### • 노드 수준 위상 특성 분석 (Nodal topological features)

다음 **8가지 노드 위상 지표(nodal topological features)**를 계산한다:

1. **노드 차수(node degree, $F_{nd}(i)$)**
2. **노드 가중합(node strength, $F_{ns}(i)$)**
3. **고유벡터 중심성(eigenvector centrality, $F_{ec}(i)$)**
4. **참여 계수(participation coefficient, $F_{pc}(i)$)**
5. **중심성(betweenness centrality, $F_{nc}(i)$)**
6. **국소 효율성(local efficiency, $F_{le}(i)$)**
7. **클러스터링 계수(weighted clustering coefficient, $F_{cc}(i)$)**
8. **노드 다기능성(nodal versatility, $F_{nv}(i)$)**

CG와 GG의 각 위상 지표 벡터 간의 **유클리디안 거리(Euclidean distance)**를 p마다 계산하여 비교하며, 결과는 $D_V(p)$로 표현된다.
사전 정규화는 Min-Max 방식으로 수행된다.

---

#### • VE 기반 모듈 내/간 연결 분석 (Intra-/Inter-modular analysis)

* **모듈 내 연결강도(intra-VE)**: $S_{\text{intra}} = \sum A_{kl}, \; k = l$
* **모듈 간 연결강도(inter-VE)**: $S_{\text{inter}} = \sum A_{kl}, \; k \ne l$

---

#### • 반구 내/간 연결 분석 (Intra-/Inter-hemispheric analysis)

* 좌반구 내부 연결: $A_{LL}$, 우반구 내부 연결: $A_{RR}$, 양반구 간 연결: $A_{LR}$
* 각 연결 강도:

$$
S_{LL} = \sum A_{LL}, \quad S_{RR} = \sum A_{RR}, \quad S_{LR} = \sum A_{LR}
$$

---

### 2.2.3 개인 수준 인지 분석 (Individual Cognitive Analyses for MSNs)

각 개인의 **IQ 점수와 MSN 특성 간의 관계**를 분석하기 위해, 두 가지 접근을 사용하였다:

1. **VE-Region 간 연결강도**
2. **전역 위상 특성(global topological features)**

분석은 **스피어만 상관계수(Spearman Correlation Coefficient, SCC)**를 사용하며, 다음과 같이 해석한다:

* $\rho > 0.2$: 유의미한 양의 관계
* $\rho < -0.2$: 유의미한 음의 관계

---

#### • VE 기반 개인 인지 분석 (Individual cognitive analysis based on VE-Regions)

* VE-Region $k$와 $l$ 사이의 연결강도를 각 피험자에 대해 계산한 벡터: $E_p(k, l)$
* 이와 IQ 벡터 $C$ 간의 SCC:

  $$
  \rho_p(E_p(k, l), C)
  $$

---

#### • 전역 위상 특성 기반 인지 분석 (Individual cognitive analysis with global topological features)

다음 **10가지 전역 위상 특성(global topological features)**과 IQ 간의 관계 분석:

1. **결합선호도(assortativity, $f_a$)**
2. **전이도(transitivity, $f_t$)**
3. **전역 효율성(global efficiency, $f_{ge}$)**
4. **특성 경로 길이(characteristic path length, $f_{cpl}$)**
5. **평균 참여 계수(mean participation coefficient, $f_{mpc}$)**
6. **평균 클러스터링 계수(mean clustering coefficient, $f_{mcc}$)**
7. **평균 다기능성(mean versatility, $f_{mv}$)**
8. **좌/우 반구 내 연결 비율(left/right intra-hemispheric ratio, $f_{lr}$)**
9. **반구 내/간 연결 비율(intra-/inter-hemispheric ratio, $f_{ii}$)**
10. **모듈 내/간 연결 비율(intra-/inter-VE ratio, $f_{VE}$)**

각 특성과 IQ 점수 간의 스피어만 상관계수:

$$
\rho_p(f_v^p, C) \quad (v \in \{a, t, ge, cpl, mpc, mcc, mv, lr, ii, VE\})
$$

---

## 3 결과 (RESULTS)

### 3.1 MSN의 집단 분석 결과 (Group Analysis Results for MSNs)

앞서 2.2.2절에서 설명한 바와 같이, 우리는 **MSN에 대한 집단 비교 분석(group comparison analyses)**을 수행하였으며, 결과는 **그림 2**에 제시되어 있다.

---

#### 3.1.1 VE-Region 기반 집단 평균 뇌 네트워크 분석 결과

(Results of VE-Region Analysis for Group Average Brain Networks)

##### • 집단 평균 네트워크 히트맵 비교 (Heatmap Comparison for Group Average Brain Networks)

그림 2a는 VE 순서대로 정렬된 **집단 평균 MSN**의 히트맵을 보여준다. 각 히트맵에서 색상의 값 범위는 -1에서 1이며, 따뜻한 색일수록 높은 값을 나타낸다. 일반적으로 MSN은 양수 및 음수 값을 모두 포함한다. 주목할 점은, CG(일반 그룹)와 GG(영재 그룹)의 평균 MSN 히트맵 간에 **뚜렷한 시각적 차이는 보이지 않는다는 점**이다.

---

##### • 상위 1% 연결의 시각적 비교 (Comparison of Top 1% Group Brain Networks)

그림 2b는 각 집단 평균 뇌 네트워크의 **상위 1% 연결(top 1%)**을 BrainNet Viewer(Xia et al., 2013)를 사용해 시각화한 것이다.

* 7개의 색 노드는 VE-Region 그룹을 나타낸다.
* **색상 링크**는 **intra-VE 연결**,
* **회색 링크**는 **inter-VE 연결**을 나타낸다.
* 노드 크기는 해당 노드의 **차수(degree)**를 반영한다.

총 308개 노드일 경우, 상위 1% 연결은 총 $\frac{(308-1)\times 308}{2} \times 1\% = 474$개의 연결이다.

**결과적으로**, GG는 CG에 비해 **intra-VE 연결이 더 많고 inter-VE 연결이 더 적다**는 시각적 차이를 보인다.

---

##### • 집단 평균 VE-Region 연결 강도 (Results of Average VE-Region Connections of Group Brain Networks)

앞서 정의한 평균 VE 연결 행렬 $E(k, l)$의 결과가 그림 2c에 나타나 있다.

* 히트맵의 대각선 값은 각 VE-Region 내부의 평균 연결 강도(intra-VE)
* 하삼각 행렬 값은 VE-Region 간의 평균 연결 강도(inter-VE)

**시각적으로**, CG와 GG 간의 평균 VE 연결 강도는 **다음 영역들에서 뚜렷한 차이(≥ 0.3)**를 보였다:

* **GG > CG**: VE 4-4 (이차 감각 영역), 4-6 (이차 감각 → 변연계 영역)
* **CG > GG**: VE 5-5 (일차 감각), 1-7 (운동 → 섬엽), 2-4 (연합 → 이차 감각)

---

##### • VE-Region 연결에서의 유의미한 차이 평가

(Significant Difference Evaluation Between CG and GG Across Each VE-Region Connections)

그림 2d는 각 VE-Region 쌍 $A_{kl}$에 대해 CG와 GG의 연결 강도 간 차이에 대한 **Mann–Whitney U 검정의 p값(Pkl)**을 시각화한 것이다.

* 유의 수준 기준 $P_{kl} < 0.05$를 만족하는 연결:

  * **VE 4-4**, **VE 1-7**, **VE 2-4**
* 준유의 수준(약간 높은 p값)에서도 의미 있는 차이:

  * **VE 1-2**, **VE 1-4**, **VE 4-6**

이는 앞서 시각화에서 관찰된 차이와 일치하며, **영재 아동(GG)**의 경우 **일부 모듈에서는 연결 강도가 증가하고, 일부는 감소**함을 나타낸다.

---

#### 3.1.2 연결 밀도 변화에 따른 집단 평균 뇌 네트워크 분석

(Analysis Results of Group Average Brain Networks Across Different Density)

그림 2e는 서로 다른 연결 밀도 $p$에 대해 **t\_p^C** (CG), **t\_p^G** (GG)의 Mann–Whitney U 검정 결과인 **z-값(zval\_p)**을 보여준다.

* $zval_p > 1.96$인 경우는 유의미한 차이를 나타냄 (신뢰수준 95%)
* **p = 0.15 \~ 0.4** 구간에서 CG와 GG 사이에 **유의미한 차이** 발생
* 최대 차이: **p = 0.3**, $zval = 2.80$

하지만 p가 0.5 이상이 되면 z-값이 안정화된다. 이는 MSNs에 **양수 및 음수 연결이 비슷한 수로 포함되어 있으며**, 음수 값은 0으로 처리되기 때문이다.

---

#### 3.1.3 연결 밀도에 따른 노드 위상 특성 변화

(Analysis Results of Nodal Topological Features in Group Networks Across Various Network Densities)

그림 2f는 각 **노드 위상 특성(nodal topological feature)**에 대해 CG와 GG의 평균 MSN 간 **유클리디안 거리(DV(p))**를 연결 밀도 $p$에 따라 시각화한 것이다.

* Dnd (노드 차수), Dns (노드 강도), Dle (국소 효율성), Dcc (클러스터링 계수), Dpc (참여 계수), Dnv (다기능성), Dnc (중심성), Dec (고유벡터 중심성)

**요약된 특징**은 다음과 같다:

* **Dnd, Dns**: p 증가에 따라 천천히 증가 → **p = 0.15\~0.3**에서 안정화
* **Dle, Dcc**: p = 0.05에서 급증 후 감소
* **Dpc**: p = 0.1에서 최고치, 이후 완만하게 감소
* **Dnv**: p = 0.01에서 최고치, 이후 지속적으로 감소
* **Dnc**: p ≤ 0.01에서만 의미 있는 값
* **Dec**: 전체적으로 낮은 값

→ **참여 계수, 국소 효율성, 다기능성** 등이 GG와 CG 구분에 유용한 지표임을 시사

---

#### 3.1.4 모듈 내/간 연결 분석 (Intra-/Inter-modular Connections Based on VE-Regions)

그림 2g는 CG 및 GG의 **intra-VE**와 **inter-VE** 연결에 대한 **바이올린 플롯(violin plot)**을 보여준다.

* 평균값은 흰 점
* 빨간색: CG, 파란색: GG

**전체적으로**:

* intra-VE > inter-VE (두 그룹 모두)
* **GG는 CG에 비해 intra-VE가 더 강하고 inter-VE는 더 약함** (그림 2h, p=0.1)

---

#### 3.1.5 반구 내/간 연결 분석 (Intra-/Inter-hemispheric Analysis)

그림 2i는 **좌반구(LL)**, **우반구(RR)**, **양반구 간(LR)** 연결에 대한 바이올린 플롯을 보여준다.

그림 2j에서는 p=0.1일 때의 각 연결 강도를 수치화하였다:

* 공통적으로:

  * **우반구(RR)** 연결 > **좌반구(LL)**
  * **양반구 간(LR)** 연결 > **반구 내 연결**

* 하지만 GG는 CG에 비해:

  * **LL 연결 강도(S\_LL)**는 더 큼
  * **RR 연결 강도(S\_RR)**는 더 작음
  * **LR 연결 강도(S\_LR)**는 약간 작음

→ **GG는 좌우 반구 내 연결 분포가 더 균형적**이라는 해석 가능

---

## 3.2 MSN의 개인 수준 인지 분석 결과

(Results of Individual Cognitive Analysis for MSNs)

앞서 2.2.3절에서 설명한 바와 같이, 본 연구는 **개인의 인지 수행(cognitive performance)**과 **형태측정 유사성 네트워크(MSN)**의 구조적 특성 간의 관계를 분석하기 위해 **스피어만 상관분석(Spearman correlation analysis)**을 수행하였다. 분석 결과는 **그림 3**에 제시되어 있다.

앞선 3.1절에서 언급한 바와 같이, MSN은 **연결 밀도(connection density) $p \geq 0.5$** 이상에서 안정성을 보인다. 그러나 본 절에서는 **$p \leq 0.6$** 범위에 집중하여 분석을 수행하였다.

---

### 3.2.1 VE-Region 기반 개인 수준 인지 분석 결과

(Results of Individual Cognitive Analysis Based on VE-Regions)

앞서 2.2.3절에서 정의된 대로, 우리는 서로 다른 연결 밀도 $p$에 대해 각 VE-Region 간의 연결 강도 $E_p(k, l)$와 **전체 IQ 점수(full-scale IQ scores)** 간의 **스피어만 상관계수(Spearman correlation coefficient, SCC)**를 계산하였다.
결과는 **그림 3a**에 나타나 있으며:

* x축: 다양한 VE-Region 연결 (예: 1-2, 4-6 등)
* y축: 상관계수 값(ρ)

#### 주요 관찰 내용:

* **낮은 연결 밀도**($p \leq 0.05$)에서는 SCC 값의 **변동성이 크고 불안정**하다.

  * 그러나 특정 연결들(예: 1-6, 3-4, 4-6)은 낮은 p에서도 **높은 상관계수**를 보인다.
* **$p \geq 0.1$** 이상에서는 상관계수가 **안정화**되며, 다음과 같은 경향이 나타난다:

  ✅ **양의 상관관계**(높은 IQ와 더 강한 연결):

  * VE 1-1 (운동 피질 내)
  * VE 2-2 (연합 피질 내)
  * VE 4-4 (이차 감각 피질 내)
  * VE 3-7 (연합 → 섬엽)
  * VE 5-6 (일차 감각 → 변연계)
  * VE 1-2 (운동 → 연합)
  * VE 4-6 (이차 감각 → 변연계)

  ❌ **음의 상관관계**(높은 IQ와 더 약한 연결):

  * VE 5-5 (일차 감각)
  * VE 1-4 (운동 → 이차 감각)
  * VE 1-7 (운동 → 섬엽)
  * VE 2-4 (연합 → 이차 감각)
  * VE 2-7 (연합 → 섬엽)
  * VE 3-4 (연합 → 이차 감각)
  * VE 4-5 (이차 감각 → 일차 감각)
  * VE 4-7 (이차 감각 → 섬엽)

---

### 3.2.2 전역 위상 특성 기반 인지 분석 결과

(Results of Individual Cognitive Analysis with Global Topological Features)

앞서 2.2.3절에서 정의된 **10개의 전역 위상 특성(global topological features)** 각각에 대해, 연결 밀도 $p$의 변화에 따른 **스피어만 상관계수 ρ**를 계산하였다.
그림 3b는 다음을 보여준다:

* x축: $p = 0.0065 \sim 1.0$ 범위의 연결 밀도
* y축: IQ와 각 특성 간의 SCC(ρ)

#### 주요 결과 요약:

✅ **IQ와 유의미한 양의 상관관계를 보인 특성들**:

* **f\_ii (반구 내 대 반구 간 연결 비율)**
  → $0.05 \leq p \leq 0.2$ 구간에서 유의미
  → 최고 상관계수: $\rho = 0.36$ (p = 0.05)
  ⇒ **높은 IQ → 더 강한 반구 내 연결, 더 약한 반구 간 연결**

* **f\_VE (모듈 내 대 모듈 간 연결 비율)**
  → 모든 p 구간에서 유의미
  → 최고 상관계수: $\rho = 0.46$ (p = 0.05)
  ⇒ **높은 IQ → 모듈 내부의 연결은 강화, 모듈 간 연결은 감소**

* **f\_lr (좌/우 반구 내 연결 비율)**
  → p = 0.1에서 유의미한 양의 상관관계
  ⇒ **높은 IQ → 좌반구 내 연결이 더 강함**

❌ **IQ와 유의미한 음의 상관관계를 보인 특성**:

* **f\_mv (평균 다기능성, mean versatility)**
  → $0.05 \leq p \leq 0.15$ 구간에서 유의미한 음의 상관관계
  ⇒ **높은 IQ → 노드가 여러 모듈에 걸쳐 속하는 경향이 감소 (더 선택적인 연결성)**

❗ **IQ와 유의미한 관계가 없거나 불안정한 특성들**:

* **f\_mpc (평균 참여 계수)**: p 변화에 따라 값이 급격히 변동 → 불안정
* **기타 전역 특성들** (f\_a, f\_t, f\_ge, f\_cpl, f\_mcc): 전 구간에서 유의미한 상관관계 없음

---

→ **요약**:

* **$p = 0.05 \sim 0.15$** 구간에서 가장 유의미한 상관관계가 관찰됨
* **높은 인지 능력**은 구조적 네트워크에서 **모듈 내 집중성, 좌반구 연결, 낮은 다기능성**과 관련 있음

---

## 4 논의 (DISCUSSION)

본 연구에서는 **sMRI 데이터**를 사용하여 **형태측정 유사성 네트워크(Morphometric Similarity Networks, MSNs)**를 계산하고, **인지 수준이 다른 아동 집단**(CG와 GG) 간의 **집단 수준(group-level)** MSN을 비교하고, **개인 수준(individual-level)** 데이터에서 **인지 수행(cognitive performance)**과 **뇌 네트워크 구조** 간의 관계를 분석하였다. 분석 결과, 다음과 같은 중요한 발견들이 도출되었다:

---

### ● 연결 밀도의 영향 (The effects of connection density)

**연결 밀도(connection density)**는 뇌 네트워크의 구조와 위상적 특성에 큰 영향을 미친다. 본 연구의 결과는 다음 두 측면에서 이 영향을 드러낸다:

1. **집단 수준 분석(group-level analysis)**

   * **CG와 GG의 차이**는 $p = 0.15 \sim 0.4$ 구간에서 더욱 뚜렷해짐.
   * **노드 위상 특성(nodal topological features)**의 유클리디안 거리 또한 $p \leq 0.05$에서 민감하게 변하며, 대부분 $p = 0.05 \sim 0.25$에서 최대치를 보임.

2. **개인 수준 분석(individual-level analysis)**

   * **VE-Region 연결과 IQ의 상관관계**는 낮은 연결 밀도($p \leq 0.05$)에서 변동성이 크고, 높은 밀도에서는 안정화됨.
   * **전역 위상 특성(global topological features)**의 상관관계는 주로 $p = 0.05 \sim 0.15$에서 최고치.

✅ 결론적으로, **$p = 0.05 \sim 0.15$**는 MSN 기반 인지 분석에서 **안정적이며 최적의 연결 밀도 범위**로 권장된다.
→ 본 연구는 **p = 0.1**에서 intra-/inter-modular 및 intra-/inter-hemispheric 분석을 수행하였다.

---

### ● 모듈 연결(VE-Region connections)과 인지 수행 간의 관계

집단 및 개인 분석 모두에서, **다음 영역 간의 연결이 높은 IQ와 양의 상관관계**를 나타냈다:

✅ 연결 강화:

* VE 4-4: **이차 감각 영역(secondary sensory area)**
* VE 1-2: **운동 → 연합 영역(motor to association area)**
* VE 4-6: **이차 감각 → 변연계 영역(secondary sensory to limbic area)**

❌ 연결 약화:

* VE 1-7: **운동 → 섬엽 영역(motor to insular area)**
* VE 2-4: **연합 → 이차 감각 영역(association to secondary sensory area)**
* VE 1-4: **운동 → 이차 감각 영역(motor to secondary sensory area)**

→ 이는 **고도의 인지 수행**이 특정 감각, 운동, 변연계 영역에서의 **연결 강화**, 일부 비효율적 경로의 **선택적 억제**와 관련되어 있음을 시사하며, **신경 효율성(neural efficiency)**의 기제를 설명할 수 있다.

---

### ● 모듈 및 반구 내/간 연결 분석 (Intra-/inter-modular and intra-/inter-hemispheric connectivity)

집단 평균 분석 결과:

* CG와 GG 모두에서 **모듈 내 연결(intra-VE)**이 **모듈 간 연결(inter-VE)**보다 강함.
* **우반구 내 연결(right intra-hemispheric)**이 **좌반구(left intra-hemispheric)**보다 강하며,
* **반구 간 연결(inter-hemispheric)**이 **반구 내 연결보다 강한 경향**이 있음 (Jiang et al., 2019과 일치)

그러나, 개인 분석에서는 **높은 IQ일수록** 다음과 같은 특징이 나타났다:

* **intra-VE 및 반구 내 연결이 강함**
* **inter-VE 및 반구 간 연결이 약함**

이는 **모듈 내 및 반구 내에서의 형태측정 유사성(morphometric similarity)**이 크고, 모듈 간/반구 간에서는 구별이 명확함을 의미한다.
→ 즉, **더 분리되고 조직화된 뇌 구조**가 **효율적인 인지 처리(efficient cognitive processing)**를 뒷받침한다(Solé-Casals et al., 2019; Santarnecchi et al., 2015; Krupnik et al., 2021).

또한, **좌/우 반구 내 연결 비율(left/right intra-hemispheric connection ratio)**이 높은 경우 IQ가 높게 나타나, **더 균형잡힌 반구 연결 분포**가 고지능과 관련이 있음을 시사한다.
※ 참고로, 이는 기존 연구(Solé-Casals et al., 2019)에서 GG가 오른쪽 반구 연결이 더 강하다고 보고한 것과는 **반대 결과**이다.

---

### ● 위상 특성과 인지 수행의 관계

(The relationship between topological features and cognitive performance)

1. **집단 분석**:

   * 일부 노드 위상 특성은 **연결 밀도 변화에 민감**함:

     * **참여 계수(F\_pc)**, **노드 다기능성(F\_nv)**, **국소 효율성(F\_le)**, **클러스터링 계수(F\_cc)**: $p = 0.05 \sim 0.1$에서 차이 최대
     * **노드 차수(F\_nd)** 및 **노드 강도(F\_ns)**: $p = 0.15 \sim 0.3$에서 안정적이며 차이 큼
   * 반면, **노드 중심성(F\_nc)**과 **고유벡터 중심성(F\_ec)**은 인지 수준을 구분하는 데 **큰 유용성을 보이지 않음**

2. **개인 분석**:

   * **평균 다기능성(mean versatility, f\_mv)**과 **IQ는 음의 상관관계** → IQ가 높을수록 각 노드는 한정된 모듈에 더 집중됨

   * 이는 기존 연구(Solé-Casals et al., 2019)에서 GG가 더 높은 다기능성을 보인 결과와 **대조적**

   * **참여 계수(f\_mpc)**는 p에 따라 상관관계가 급변 → **신뢰도 낮음**

---

### ● 한계점 (Limitations)

1. **표본 수가 적음(n=29)** → 일반화에 제약 → 향후 더 큰 집단 필요
2. **MSN의 음수 값은 0으로 처리**됨 → 네트워크 구조 해석에 왜곡 가능성
3. 본 연구는 **구조적 네트워크(structural networks)**에 초점을 두었으며, **기능적 영상(functional imaging)** 통합 시 생리학적 및 인지적 해석을 더욱 풍부하게 할 수 있음

---

## 5 결론 (CONCLUSIONS)

본 연구에서는 **sMRI(구조적 자기공명영상)** 데이터를 기반으로 **형태측정 유사성 네트워크(Morphometric Similarity Networks, MSNs)**를 구축하여, **인지 수준이 다른 아동**들의 뇌 네트워크 특성을 조사하였다.
우리는 두 가지 수준의 분석을 수행하였다:

1. **집단 수준 분석(group-level analysis)**:

   * 일반 그룹(CG)과 영재 그룹(GG)의 평균 MSN을 비교하여 뇌 네트워크 위상(topology)의 주요 차이를 식별함.

2. **개인 수준 분석(individual-level analysis)**:

   * 인지 수행(cognitive performance)과 뇌 네트워크 구조 간의 관계를 탐색함.

---

### 주요 결과는 다음과 같다:

* **연결 밀도(connection density)의 변화**는

  * **전역(global)** 및 **노드 수준(nodal)**의 위상적 특성에 **중대한 영향**을 미친다.
  * 연결 밀도가 다를 때, 각 위상 특성은 **상이한 변화 양상(distinct trends)**을 나타낸다.
    ✅ 따라서 **MSN 기반 인지 분석에서는 p = 0.05 \~ 0.15** 구간이 **안정적이고 최적의 결과**를 제공함.

* **영재 아동(GG)**은 다음과 같은 구조적 특징을 나타냄:

  * **반구 내 연결(intra-hemispheric connectivity)** 및 **모듈 내 연결(intra-modular connectivity)**이 더 강함
  * **반구 간 연결(inter-hemispheric connectivity)** 및 **모듈 간 연결(inter-modular connectivity)**은 더 약함
  * **좌우 반구 내 연결의 분포**가 더 균형적임
  * **평균 다기능성(mean versatility)**이 더 낮음

  → 이러한 구조는 **보다 효율적이고 안정적인 인지 처리(efficient and stable cognitive processing)**와 연관되어 있을 수 있음.

* **VE 기반 해부학적 모듈성 분석(anatomical modularity analysis based on von Economo)** 결과:

  ✅ 높은 인지 수행은 다음과 관련됨:

  * **특정 모듈**에서의 **연결성 증가**

    * 예: **이차 감각 영역(secondary sensory area)**,
      **운동 → 연합 영역(motor to association area)**,
      **이차 감각 → 변연계 영역(secondary sensory to limbic area)**

  ❌ 반면, **일부 모듈 간 연결**은 선택적으로 **감소**

  * 예: **운동 → 섬엽 영역(motor to insular area)**,
    **연합 → 이차 감각 영역(association to secondary sensory area)**,
    **운동 → 이차 감각 영역(motor to secondary sensory area)**

  → 이는 **더 큰 신경 효율성(neural efficiency)**을 유도할 수 있음.

* **특정 위상 특성(topological features)**은 인지 수행과 유의미하게 연관됨:

  * 유용한 특성들:

    * **참여 계수(participation coefficient)**
    * **노드 다기능성(nodal versatility)**
    * **국소 효율성(local efficiency)**
    * **클러스터링 계수(clustering coefficient)**
      → 이들은 특정 연결 밀도에서 IQ와 상관관계를 가짐

  * 비신뢰적인 특성들:

    * **평균 참여 계수(mean participation coefficient)**: p에 따라 상관성이 급변함
    * **결합 선호도(assortativity)**
    * **특성 경로 길이(characteristic path length)**
    * **가중 클러스터링 계수(mean weighted clustering coefficient)**
      → 이들은 IQ와의 유의미한 상관관계를 보이지 않음

---

### 결론적으로, 본 연구는 다음을 강조한다:

* **연결 밀도의 영향**은 매우 중요하며,
* **모듈 연결성(modular connectivity)**,
* **반구 연결성(hemispheric connectivity)**,
* **특정 위상 특성(topological features)**은
  → **아동의 인지 수행(cognitive performance)**과 밀접하게 연관됨.

이러한 결과는 향후 연구에서 **인지 능력의 신경 기제(neural mechanisms)**를 심층적으로 탐색할 수 있는 토대를 제공한다.

✅ 또한, 향후에는 다음과 같은 방향의 연구가 필요하다:

* 더 **크고 다양한 표본 집단(large and diverse samples)** 사용
* **종단 연구 설계(longitudinal designs)** 도입
  → 이를 통해 **인지 발달(cognitive development)**에 따른 **뇌 네트워크 위상(topology)**의 진화 양상을 이해하고,
  → **인간 지능(human intelligence)**의 **신경학적 기반(neural basis)**을 보다 정밀하게 규명할 수 있을 것이다.

---

## 감사의 말 (ACKNOWLEDGEMENTS)

본 연구는 **카탈루냐 중앙대학교(University of Vic – Central University of Catalonia)**의 **실험 과학 및 기술 박사과정(Doctoral Programme in Experimental Sciences and Technology)**의 일환으로 수행되었다.

* **F.D. (Feng Duan)**의 연구는 다음의 지원을 일부 받았다:

  * **중국 국가자연과학재단(National Natural Science Foundation of China)**의 **핵심 과제(Key Program)** (과제번호: 11932013)
  * **톈진 과학기술기획 프로젝트(Tianjin Science and Technology Plan Project)** (과제번호: 22PTZWHZ00040)

* **C.F.C. (Cesar F. Caiafa)**의 연구는 다음의 아르헨티나 기반 연구비 지원을 일부 받았다:

  * **PICT 2020-SERIEA-00457**
  * **PIP 112202101 00284CO**

---

## 참고문헌 일부 (REFERENCES) – 번역 예시

> ※ 참고문헌은 전체 번역보다는 필요한 부분에 대한 **출처 확인** 또는 **인용 목적**이 주로 중요합니다. 다만 요청에 따라 대표 항목 몇 개를 예시로 번역해드립니다.

---

**Blondel et al. (2008)**

> Blondel, V. D., Guillaume, J.-L., Lambiotte, R., & Lefebvre, E. (2008).
> **대규모 네트워크에서의 커뮤니티 탐지(Fast unfolding of communities in large networks).**
> *Journal of Statistical Mechanics: Theory and Experiment*, 2008(10): P10008.

---

**Fischl & Dale (2000)**

> Fischl, B., & Dale, A. M. (2000).
> **자기공명영상으로 인간 대뇌 피질의 두께 측정( Measuring the thickness of the human cerebral cortex from magnetic resonance images).**
> *Proceedings of the National Academy of Sciences*, 97(20): 11050–11055.

---

**Seidlitz et al. (2018)**

> Seidlitz, J., Vása, F., Shinn, M., Romero-Garcia, R., Whitaker, K. J., Vértes, P. E., et al. (2018).
> **형태측정 유사성 네트워크는 미세한 피질 구조를 탐지하고 개인 간 인지 변이를 예측한다(Morphometric similarity networks detect microscale cortical organization and predict inter-individual cognitive variation).**
> *Neuron*, 97(1): 231–247.

---

**Santarnecchi et al. (2015)**

> Santarnecchi, E., Tatti, E., Rossi, S., Serino, V., & Rossi, A. (2015).
> **지능과 관련된 자발적 대뇌 활동의 비대칭성(Intelligence-related differences in the asymmetry of spontaneous cerebral activity).**
> *Human Brain Mapping*, 36(9): 3586–3602.

---
