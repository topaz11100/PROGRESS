**"Unveiling the core functional networks of cognition: An ontology-guided machine learning approach"**

---

### 초록 (Abstract)

다양한 인지 기능(cognitive functions)의 기반이 되는 기능적 구조(functional architecture)를 해독하는 일은 신경과학(neuroscience)의 근본적인 과제이다. 본 연구에서는 인지 온톨로지(cognitive ontology)와 기능 연결성 분석(functional connectivity analysis)을 통합한 혁신적인 머신러닝(machine learning) 프레임워크를 활용하여 인지에 필수적인 뇌 네트워크(brain networks)를 식별하였다. 우리는 주로 연합 피질(association cortex)에 위치한 핵심 기능 연결망(functional connectomes)을 확인하였으며, 이는 다양한 인지 영역(cognitive domains)에 걸쳐 기존 연구에서 널리 사용된 두 가지 전통적인 방법들보다 뛰어난 예측 성능(predictive performance)을 보였다. 본 접근법은 작업 기억(working memory), 독해력(reading comprehension), 지속적 주의(sustained attention)를 포함한 16가지 인지 과제에서 평균 0.13의 측 정확도(mean prediction accuracy)를 기록하여, 전통적 방법의 0.08보다 우수하였다. 반면, 본 방법은 감각(sensory), 운동(motor), 감정(emotional) 기능에 대해서는 예측력이 제한적이었으며, 관련된 9가지 과제에서 평균 0.03의 예측 정확도를 보였고 이는 전통적 방법의 0.04보다 다소 낮았다. 이러한 인지 연결망(cognitive connectomes)은 휴식 상태 기능 연결(resting-state functional connectivity), 백질 경로(white matter tracts)를 통한 구조적 연결성(structural connectivity), 그리고 유전자 발현(gene expression)의 독특한 패턴으로 특징지어졌으며, 이들의 신경유전학적 기반(neurogenetic underpinnings)을 강조하였다. 우리의 연구 결과는 인지에 핵심적인 범영역적 기능 네트워크 지문(domain-general functional network fingerprint)을 밝혀내며, 인지 능력(cognitive abilities)의 신경적 기초를 탐색하기 위한 새로운 계산적 접근법(computational approach)을 제시한다.

---

### 1. 서론 (Introduction)

인간의 마음(human mind)의 복잡성을 해명하기 위해서는 주의(attention), 기억(memory), 실행 기능(executive functions), 언어(language), 사회적 인지(social cognition)와 같은 인지 기능(cognitive functions)에 대한 심층적인 탐구가 필요하다. 이러한 기능들은 서로 얽혀 있으며, 신경과학(neuroscience)을 이해하는 데 있어 기초적이다(Cosmides and Tooby, 2013; Harvey, 2019; Schöttner et al., 2023). 인지 온톨로지(cognitive ontology)의 등장으로 이러한 정신 능력(mental capacities)을 구조적으로 탐색할 수 있는 길이 열렸고, 이들의 복잡한 상호관계를 데이터 기반 접근(data-driven approach)을 통해 지도화(mapping)할 수 있게 되었다(Burgoyne et al., 2022; Burkart et al., 2017; McGrew, 2009; Murtazina and Avdeenko, 2021; Poldrack and Yarkoni, 2016). 그러나 인지 온톨로지의 구성에 대한 발전에도 불구하고, 그 신경적 기초(neural underpinnings)를 밝히는 일은 여전히 중요한 과제로 남아 있다.

최근 연구들은 다양한 뇌 영역(brain regions) 간 BOLD 시계열(BOLD time series)의 상관관계인 기능 연결성(functional connectivity, FC)을 활용하여 인지 능력(cognitive abilities)을 예측하는 데 성공을 거두었으며, 뇌의 조직 원리(organizational principles)에 대한 통찰을 제공하였다(Chen et al., 2022; Dubois et al., 2018; R. Kong et al., 2023; Tian et al., 2020). 하지만 연구 간 결과의 불일치는 인지 온톨로지 항목(cognitive ontology entity)에 대한 통합적인 신경 기반(unified neural basis)을 흐리게 하고 있다(Dubois et al., 2018; R. Kong et al., 2023; D. Kristanto et al., 2023; Liu et al., 2020; Rong Wang et al., 2021; Tian and Zalesky, 2021). 특히 인지 요인(cognitive factors)을 예측할 때, 어떤 연구들은 각각의 네트워크(network)가 유사한 기여를 한다고 보고한 반면(Dubois et al., 2018; Liu et al., 2020), 다른 연구들은 기본 모드 네트워크(Default Mode Network, DMN), 주의 네트워크(attention networks), 전두두정 제어 네트워크(frontoparietal control network, FPCN), 그리고 주목 네트워크(salience network)가 더 큰 기여를 한다고 보고하였다(D. Kristanto et al., 2023).

이러한 불일치에도 불구하고, 최근 연구들은 특정 뇌 네트워크(brain networks)가 다양한 인지 기능을 지원하는 데 핵심적 역할을 한다는 점을 강조하고 있다. Bolt et al. (2017)은 탐색적 이요인 분석(exploratory bifactor analysis)을 통해 “집중된 인식(focused awareness)” 혹은 “주의 에피소드(attentional episode)”를 나타내는 일반 요인(general factor)을 규명하였으며, 이는 인지, 지각(perception), 행동(action), 감정(emotion) 영역 전반에 걸친 범영역적 심리 과정(domain-general psychological process)을 상징하며, 과제-양성 네트워크(task-positive network)의 핵심 영역(core regions)에 나타났다. 한편, Kristanto et al. (2022)은 뇌 유래 온톨로지(neurometric ontology)와 인지 수행 기반 온톨로지(psychometric ontology) 간의 정렬(alignment)을 조사하여, 인지 능력과 관련된 뇌 영역들이 광범위하게 상호 연결된 구조적 네트워크(structural network)를 형성함을 밝혔다. 이러한 발견은 특정 뇌 영역이 인지 기능에 중요하다는 점을 강조하며, 일부 기능 연결성(connectome)이 인지를 지원하는 데 결정적인 역할을 한다는 본 연구의 가설(hypothesis)의 기반이 된다.

이러한 가설을 더욱 뒷받침하는 연구로는, 인지 요인이 여러 인지 영역에서 예측력을 지니며 개인의 이념적 성향 차이(ideological preferences)와도 관련이 있음을 보여주는 연구들이 있다(Burgoyne et al., 2022; Cosmides and Tooby, 2013; McGrew, 2009; Schöttner et al., 2023). He et al. (2022)은 대규모 데이터셋(UK Biobank, N=36,848)에서 구축된 예측 모델을 보다 소규모(Human Connectome Project, HCP, N=1019)의 비-뇌영상(non-brain-imaging) 표현형에 적용하는 메타 매칭 프레임워크(meta-matching framework)를 제시하여, 기능 연결성(FC) 데이터의 예측력을 입증하였다. 이러한 결과에 고무되어, 우리는 FC 네트워크가 인지 요인을 포착하고 초기 연구 집단을 넘어 다양한 인지 기능을 예측할 수 있는 능력을 탐색하고자 하였다.

그러나 이러한 고무적인 결과에도 불구하고, 기존 연구들은 인지 요인을 구성하기 위해 서로 다른 과제(task)와 방법(method)을 사용하였다(Chen et al., 2022; Dubois et al., 2018; R. Kong et al., 2023; Tian et al., 2020). 이러한 불일치는 인지 요인을 예측하는 데 있어 동일한 연결(edge)이 중요한 기여를 했는지 여부를 직접적으로 비교하는 데 어려움을 초래한다(Dubois et al., 2018; R. Kong et al., 2023; Kristanto et al., 2022; D. 2023). 따라서 우리는 서로 다른 방법으로 구성된 인지 요인이 유사한 기능 연결망(functional networks)에 의해 예측될 수 있는지를 조사하고, 그 예측 정확도(prediction accuracy)가 서로 다른지를 확인함으로써 FC와 인지 요인 간의 일반적인 관계를 규명하고자 한다.

더 나아가, 다양한 인지 과제로부터 파생된 잠재 변수(latent variable)로서의 인지 요인은 여러 영역에서의 수행을 뒷받침하는 범영역적 인지 능력(domain-general cognitive ability)을 반영할 가능성이 있다. 따라서 인지 요인을 효과적으로 나타내는 FC 연결망(connectome)은 주의, 작업 기억, 실행 제어(executive control), 언어 처리(language processing)를 포함한 다양한 인지 기능에서 개인차를 예측할 수 있어야 한다(Francken et al., 2022; Murtazina and Avdeenko, 2021). 우리는 특정 FC 연결망이 실행 기능이나 언어와 같은 인지 기능은 잘 나타내는 반면, 운동(motor) 기능이나 감정(emotion)과 같이 인지와 덜 관련된 기능은 그렇지 않을 것이라 가정하였다. 이 가설은 다양한 인지 영역과 데이터셋에서 FC 데이터의 예측력을 보여주는 최근 연구들과도 일치한다(Chen et al., 2022; Gholipour et al., 2022; L. He et al., 2021). 또한, 우리는 인지 요인을 나타내는 데 중요한 FC 네트워크들이 주로 연합 피질(association cortex) 내의 연결로 구성되어 있을 것이라 가정하였다. 연합 피질은 전전두엽 피질(prefrontal cortex), 두정엽 피질(parietal cortex), 측두엽 피질(temporal cortex) 등의 영역을 포함하며, 주의, 작업 기억, 의사결정, 언어 등 고차원 인지 처리(higher-order cognitive processes)와 관련이 있다. 이러한 영역들은 높은 수준의 기능 연결성을 보이며, 정보의 통합 및 처리를 지원하는 고도로 상호 연결된 네트워크를 형성한다(Cui et al., 2020; Gordon et al., 2020; L. He et al., 2021; Tian and Zalesky, 2021).

우리는 HCP 청년(HCP-YA, Van Essen et al., 2013) 및 HCP 발달(HCP-D, Somerville et al., 2018) 연구의 행동 및 휴식 상태 fMRI 데이터를 활용하여, 서로 다른 방법으로 구성된 인지 요인을 특정 기능 네트워크가 일관되게 예측할 수 있는지, 그리고 이러한 네트워크가 실제 인지 행동(cognitive behaviors)을 예측할 수 있는지를 검증하였다. 이러한 접근은 해당 네트워크의 예측 안정성(predictive stability)을 검증할 뿐만 아니라, 인지 요인과 연관된 FC 네트워크의 생물학적 기초(biological basis) — FC 강도 변동성(variability), 백질 연결성(white matter connectivity), 유전자 연관성 패턴(gene association patterns) — 을 심층적으로 탐구하였다. 본 연구의 종합적인 접근은 기능 연결성(functional connectivity), 구조 연결성(structural connectivity), 유전자 발현(gene expression), 그리고 인지(cognition) 간의 복잡한 상호작용을 해명하고자 하며, 인간의 지능(intelligence)과 행동(behavior)의 신경적 기반에 대한 이해를 심화시키는 데 목적이 있다.

---

### 2. 방법 (Method)

#### 2.1 참여자 정보 (Participant Information)

본 연구에서는 두 개의 데이터셋을 사용하였다: WU-Minn HCP-YA S1200 릴리스(Van Essen et al., 2013)와 HCP-D(Somerville et al., 2018). HCP-YA 데이터셋은 주요 가설, 즉 인지 요인(cognitive factor)의 기반이 되는 고유한 네트워크 기능 연결성 엣지(functional connectivity edges) 집합이 인지 관련 행동(cognitive-related behaviors)을 예측할 수 있는지, 반면 인지와 덜 관련된 행동(less-related behaviors)은 그렇지 않은지를 검증하는 데 사용되었다. HCP-D 데이터셋은 이러한 고유한 네트워크 구성이 서로 다른 데이터셋에서도 유사한 예측력을 갖는지를 평가하기 위해 사용되었다. 데이터 수집 프로토콜에 대한 자세한 내용은 HCP 프로젝트 웹사이트([https://www.humanconnectome.org/)를](https://www.humanconnectome.org/%29를) 참조하라. 본 프로젝트는 워싱턴 대학교(Washington University) 지역 윤리위원회의 승인을 받았다.

HCP-YA S1200 릴리스의 공개 접근 가능한 데이터를 사용하였으며, 여기에는 휴식 상태 기능적 MRI(resting-state fMRI), 확산 MRI(diffusion MRI), 구조적 MRI(structural MRI) 등 다양한 자기공명영상(MRI) 방식이 포함되어 있다. 영상 데이터는 Siemens 3T Skyra 스캐너와 멀티밴드(multiband) 시퀀스를 사용하여 획득되었으며, 각 참여자는 서로 다른 날에 두 번의 fMRI 세션을 수행하였고, 각 세션은 왼쪽-오른쪽 및 오른쪽-왼쪽(LR/RL)의 위상 인코딩 러닝을 포함하였다. T1-가중 구조 영상(T1-weighted structural image)은 각 참여자당 하나의 0.7 mm 등방성(isotropic) 스캔으로 이루어졌다. 확산 MRI(dMRI) 데이터는 각 참여자당 여섯 번의 1.25 mm 등방성 러닝으로 구성되었다. 데이터셋과 MRI 획득 파라미터에 대한 더 많은 정보는 이전 연구(Van Essen et al., 2013)를 참고하라.

영상 데이터 외에도 HCP 데이터베이스는 다양한 인지 과제(cognitive tasks)에 대한 인구통계 정보와 수행 지표(performance metrics)를 제공한다. 본 연구 당시 HCP 데이터베이스에 등록된 1206명의 참여자 중에서, 정보가 불완전하거나, fMRI 이미지가 부족하거나, 움직임 기준에 부적합하거나, 왼손잡이(left-handed)인 참여자들은 제외되었다(Bailey et al., 2020). 결과적으로 최종 분석에 포함된 표본은 601명(여성 329명; 연령 22–36세)이다.

본 연구에서는 또한 HCP-D의 Lifespan 2.0 릴리스에서 총 633명의 피험자(남성 294명, 연령 8–21세)를 포함하였다. 모든 영상 데이터는 3T Siemens Prisma 스캐너에서 멀티밴드 EPI 시퀀스를 사용하여 수집되었다. 각 참여자는 서로 다른 날에 두 번의 휴식 상태 fMRI(rs-fMRI) 세션에 참여하였으며, 총 4회의 러닝이 수행되어 26분 분량의 rs-fMRI 데이터를 구성하였다. T1-가중 구조 영상은 참여자당 하나의 0.8 mm 등방성 스캔으로 수집되었다. 데이터셋과 MRI 획득 파라미터에 대한 자세한 정보는 Somerville et al. (2018)을 참고하라.

불완전한 정보, fMRI 이미지 부족, 움직임 기준 미달, 왼손잡이인 참여자들은 제외되었으며(Bailey et al., 2020), 이에 따라 최종 분석 표본은 374명(여성 197명; 연령 8–22세)으로 구성되었다.

---

### 2.2 fMRI 데이터의 전처리 및 기능 연결성 추정

(The pre-processing of fMRI data and functional connectivity estimation)

본 연구에서는 HCP-D 및 HCP-YA 양쪽 모두에서 최소 전처리된(minimally preprocessed) T1-가중(T1w) 이미지와 fMRI 이미지를 사용하였다. T1w 이미지는 우선적으로 강도 불균일(intensity non-uniformity)에 대해 보정되었고, 이후 전체 워크플로우 동안 T1w 기준 참조 이미지(T1w-reference)로 활용되었다. 두개골 제거(skull-stripping)와 뇌 표면 재구성(brain surface reconstruction)을 거친 후, 체적 기반의 뇌 추출 T1w 이미지는 뇌척수액(cerebrospinal fluid, CSF), 백질(white matter, WM), 회백질(gray matter, GM)로 분할(segmentation)되었고, 이후 MNI 공간(MNI space)으로 공간 정규화(spatial normalization)되었다.

rs-fMRI 이미지는 움직임 보정(motion correction), 왜곡 보정(distortion correction), T1w 기준 이미지에 대한 공동 정합(co-registration), MNI 공간으로의 정규화(normalization) 등의 전처리 과정을 거쳤다(Glasser et al., 2013). 이후 BOLD 시계열(BOLD timeseries)은 fsaverage 공간으로 재샘플링되어 91,000개의 샘플을 포함한 회색 좌표(grayordinates) 파일이 생성되었다.

전처리된 fMRI 이미지는 이후 **XCP-D(Extensible Connectivity Pipelines)** (Ciric et al., 2018)을 이용하여 추가 후처리(post-processing)를 수행하였다. 잡음 회귀(nuisance regression) 이전에, 프레임 변위(framewise displacement, FD)가 0.3을 초과한 볼륨은 이상치(outliers)로 간주되어 제외되었다. 총 36개의 잡음 회귀 변수(nuisance regressors)가 BOLD 데이터에서 회귀 제거되었는데, 여기에는 움직임 파라미터(motion parameters), 전역 신호(global signal), 평균 백질(mean white matter) 및 평균 CSF 신호(mean CSF signal), 이들의 시간 미분(temporal derivatives), 그리고 이들에 대한 2차 확장(quadratic expansion) 등이 포함된다. 이후 남은 시계열은 0.01–0.08Hz 대역 통과 필터(band-pass filter)를 적용하고, FWHM = 6mm로 공간 평활화(spatial smoothing)하였다(Ciric et al., 2017; Satterthwaite et al., 2013).

머리 움직임(head motion)의 잠재적 영향을 줄이기 위해, 다음 두 기준을 기반으로 추가적인 참여자 제외 조치를 취하였다(Faskowitz et al., 2020; Rosenthal et al., 2018).

1. fMRI 데이터 중 하나라도 러닝 내에서 FD의 25% 이상이 0.2mm를 초과하면 해당 참여자는 제외하였다.
2. fMRI 데이터의 평균 FD가, 각 데이터셋의 동일한 러닝에 대해 산출된 평균 FD의 사분위수 간 범위(interquartile range, IQR)의 1.5배를 초과할 경우, 해당 참여자를 제외하였다.

최종적으로, HCP-YA에서는 4개의 rs-fMRI 러닝 모두가 있는 601명의 참여자(여성 329명, 연령 22–36세), HCP-D에서는 4개의 rs-fMRI 러닝을 모두 만족하는 374명의 참여자(여성 197명, 연령 8–22세)가 분석에 포함되었다.

우리는 **Schaefer parcellation(Schaefer et al., 2018)**을 사용하여 각 영역(region)의 BOLD 시계열 데이터를 추출하였다. 이 분할(parcellation)은 전체 뇌를 400개의 영역(parcels)으로 나누며, 기존 연구에서 널리 사용되어 왔다(Kong et al., 2021; Yang et al., 2023). 기존 연구들은 이 parcellation이 인지 기능 예측을 위한 기능 연결성 분석(context of FC network analysis)에서 뛰어난 성능을 보였음을 입증하였다(Gholipour et al., 2022; Kong et al., 2021). 우리는 각 parcel의 시계열 간 피어슨 상관 계수(Pearson correlation coefficient)를 계산하여 기능 연결성(functional connectivity, FC)을 평가하였다. 그 결과, 각 참여자에 대해 대칭적인 400 × 400 기능 연결성 행렬(functional connectivity matrix)을 얻을 수 있었고, 이를 Fisher 변환(Fisher transformation) 후, 상삼각 행렬(upper triangle)을 벡터화하여 총 79,800개의 연결성 특징(connectivity features)을 생성하였다.

---

### 2.3 인지 요인 계산 (Cognitive factor computation)

심리측정적 온톨로지 항목(psychometric ontological entity)을 도출하기 위해, 우리는 HCP-YA 데이터셋의 행동 데이터(behavioral data)를 기반으로 확인적 요인 분석(confirmatory factor analysis, CFA) 모델을 수행하였다. CFA는 온톨로지 항목(ontological entity)을 강건하게 구축하는 데 사용될 수 있는 통계적 기법이다(Dubois et al., 2018; Kristanto et al., 2022; Schöttner et al., 2023). 우리는 이전 연구들에 따라, fMRI 기반 과제 수행 측정값(in-scanner test), NIH Toolbox, Penny Cognitive Battery에서 유래한 13개의 행동 지표(behavioral metrics)를 선택하였다(Dubois et al., 2018; Kristanto et al., 2022; Schöttner et al., 2023). 이들 지표는 다음과 같은 5개의 상이한 인지 영역(cognitive domains)을 포함한다:

1. **처리 속도와 관련된 실행 기능(executive functions related to processing speed)**:

   * NIH 미보정 척도 점수(NIH unadjusted scale score)

     * *Dimensional Change Card Sort*
     * *Flanker test*
     * *Pattern Completion Processing Speed*

2. **작업 기억과 관련된 실행 기능(executive functions associated with working memory)**:

   * 2-back 조건에서의 반응 시간(Reaction time)
   * *List Sorting task*
   * *Picture Sequence Memory*

3. **유동성 지능(fluid intelligence)**:

   * \*Penn Progressive Matrices (PMAT24)\*에서

     * 정확한 응답 수(Number of Correct Responses, PMAT24 A CR)
     * 생략된 항목 수(Total Skipped Items, PMAT24 A SI)
     * 정답 반응의 중앙 반응 시간(Median Reaction Time for Correct Responses, PMAT24 A RTCR)

4. **관계 유추 능력(relation ability)**:

   * *Relation task*에서

     * 일치 조건(match condition)의 반응 시간
     * 관련성 조건(relevance condition)의 반응 시간

5. **언어 능력(language ability)**:

   * NIH 미보정 점수

     * *Picture Vocabulary test*
     * *Reading Recognition test*

해당 과제들의 요약은 **표 1**에 정리되어 있다.

인지 온톨로지 요인을 도출하기 위한 방법에는 여러 가지가 있으며, 인지 온톨로지 항목(cognitive ontology entity)을 정의하기 위한 포괄적 합의(comprehensive consensus framework)는 아직 수립되지 않았다(Francken et al., 2022; Murtazina and Avdeenko, 2021; Poldrack and Yarkoni, 2016). 하지만, 선행 연구들에 따르면 실행 기능(executive functions), 유동성 지능(fluid intelligence), 언어 능력(language abilities) 등은 독립적인 것이 아니라, 계층적 인지 구조(hierarchical cognitive organization)를 보여준다고 보고되었다(Schöttner et al., 2023). 이에 따라, 우리는 범영역적(domain-general) 인지 온톨로지 항목을 구축하기 위해 **2차 요인(confirmatory second-order factor) 모델**을 제안하였다.

이를 위해, 우리는 R 소프트웨어([https://www.r-project.org/](https://www.r-project.org/)) 내의 **lavaan 패키지**([https://lavaan.ugent.be)를](https://lavaan.ugent.be%29를) 사용하였다.

우리는 모든 13개의 과제 점수가 다음의 5개 1차 요인(first-order factors)으로 조직될 수 있다고 가정하였다:

* 처리 속도 관련 실행 기능
* 작업 기억 관련 실행 기능
* 관계 유추 능력
* 유동성 지능
* 언어 능력
  또한, 선행 연구(Schöttner et al., 2023)의 탐색적 요인 분석(EFA) 결과를 바탕으로, 이들 5개의 1차 요인 간의 상호 관계를 포착할 수 있는 **2차 잠재 변수(latent variable)**인 ‘인지 요인(cognitive factor)’을 추가로 설정하였다. 이 모델은 총 601명의 HCP-YA 참여자 데이터를 기반으로 적합(fit)되었다. 모델 식별(model identification)을 원활히 하기 위해, 모든 행동 점수는 z-점수(z-score)로 표준화되었고, 모든 요인 부하량(factor loadings)은 자유롭게 추정되도록 설정하였다.

CFA 모델은 최대우도 추정(Maximum Likelihood, ML) 방법으로 평가되었으며, 모델 적합도(model fit)는 다음의 지표들을 기반으로 평가되었다:

* 카이제곱 적합도 지수(χ²)
* 비교 적합도 지수(Comparative Fit Index, CFI)
* 평균 제곱 근 근사 오차(Root-Mean-Squared Error of Approximation, RMSEA)
* 표준화된 평균 제곱 근 잔차(Standardized Root-Mean-Squared Residual, SRMR)

우리는 기존 권고안(Hu and Bentler, 1999)을 따라, CFI ≥ 0.95, RMSEA 및 SRMR < 0.08일 때 양호한 적합도로 간주하였다. 모델 적합 후, 우리는 **lavPredict 함수**(Rosseel, 2012)를 이용한 회귀 방법(regression method)을 통해 개별 수준(individual-level)의 인지 요인 점수(cognitive factor score)를 계산하였다.

---

### 2.4 기능 연결성(FC)을 이용한 인지 요인 점수 예측

(Prediction of the cognitive factor score using FC)

인지 요인 점수(cognitive factor score) 예측에 유의미하게 영향을 미치는 기능 연결성 엣지(functional connectivity edges)를 식별하기 위해, 우리는 **릿지 회귀(ridge regression)**를 사용하여 CFA 모델로부터 도출된 인지 요인 점수와 모든 FC 엣지 간의 관계를 분석하였다(Cui et al., 2020; Cui and Gong, 2018; Kong et al., 2023; Tian and Zalesky, 2021).

2차 인지 요인 점수(second-order cognitive factor score)를 종속 변수(dependent variable)로 설정하여, 각 엣지에 해당하는 회귀 계수(β 값)를 계산하였다. 릿지 회귀의 L2-노름 정규화(L2-norm regularization)는 학습 오차(training error)와 모델 복잡도(model complexity) 간의 균형을 이루도록 하였다. 각 엣지의 β 계수의 크기(magnitude)는 인지 요인 예측에서 해당 엣지의 중요도를 나타낸다.

우리는 모든 β 계수의 절댓값을 정렬한 뒤, 상위 10%에 해당하는 엣지를 선택하였다. 이를 통해, 인지 요인 점수를 예측하는 데 핵심적인 FC 엣지 하위집합(subset)을 식별하였다. 또한, Haufe et al. (2014)에서 제안한 방법을 사용해 β 계수를 변환(transform)한 후, 동일하게 상위 10% 엣지를 선택하였다. Haufe 변환은 다변량 해독 모델(multivariate decoding model)을 해석 가능한 활성화 패턴(interpretable activation pattern)으로 변환하며, 선형 해독 모델에서의 가중치 맵(weight map)이 실제 신경 활동을 정확히 반영하지 못하는 문제를 해결한다(Chen et al., 2023; Haufe et al., 2014; Tian and Zalesky, 2021). 이 접근은 특히 신경영상(neuroimaging) 연구에서 공간적 정보 분포의 오해를 줄이는 데 유용하다.

릿지 회귀 모델 학습에는 **중첩된 2-폴드 교차검증 전략(nested 2-fold cross-validation strategy)**을 사용하였다. 각 반복(iteration)마다 데이터셋을 훈련 세트(training set)와 검증 세트(validation set)로 나누었으며(Cui et al., 2020), 예측 정확도(prediction accuracy)는 실제 값과 예측값 간의 피어슨 상관 계수(Pearson correlation coefficient) 및 평균 제곱 오차(Mean Squared Error, MSE)를 통해 평가하였다. 각 반복에서 훈련 세트와 테스트 세트의 역할을 교체하였으며, 두 개의 R 값(상관 계수)과 두 개의 MSE 값을 생성하였다. 우리는 모델의 전반적인 성능을 평가하기 위해 이러한 값을 100회 반복하여 평균하였다.

이때, ‘예측 정확도(prediction accuracy)’는 별도의 정의가 없는 한, 실제값과 예측값 간의 피어슨 상관 계수(R)를 의미한다. 모델 가중치(β 계수)는 100회 반복에서 평균하여, 반복 간의 일관성과 엣지의 안정성을 확보하였다. 이러한 방식은 계산 모델링(computational modeling)에서 단일 반복의 임의성(random fluctuation) 또는 노이즈를 줄이기 위한 통계적 안정성 확보 방법으로 정당화된다(Cui et al., 2018, 2020; Cui and Gong, 2018).

FC 엣지가 인지 요인 점수를 유의미하게 예측하는지 여부를 평가하기 위해, 우리는 **퍼뮤테이션(permutation) 테스트**를 기반으로 영가설(null hypothesis) 하에서의 분포를 생성하였다. 이를 위해 훈련 세트 내의 인지 요인 점수를 무작위로 200회 셔플하여, FC와 인지 요인 간에 관계가 없다는 가정 하에서의 예측 정확도 샘플 200개를 생성하였다. 이후 위에서 얻은 100개의 실제 R 값을 이 영분포와 비교하기 위해 **비모수 윌콕슨 부호 순위 검정(Wilcoxon signed-rank test)**을 수행하였다(Tian et al., 2020; Tian and Zalesky, 2021).

---

### 2.5 교차 과제 예측 패러다임에서 사용된 행동

(Behaviors used in cross task prediction paradigm)

인지 요인 점수(cognitive factor score)를 예측하는 데 핵심적인 기능 연결성 엣지(functional connectivity edges)가 실제 인지 기능(cognitive functions)을 효과적으로 나타내는지를 평가하기 위해, 우리는 **HCP-YA 데이터셋**에서 25개의 행동 지표(behavioral metrics)를 선택하여 **교차 과제 예측 패러다임(cross-task prediction paradigm)**에 적용하였다. 이 타겟 행동들은 작업 기억(working memory), 유동성 지능(fluid intelligence), 언어 능력(language ability), 공간 주의(spatial attention), 지속적 주의(sustained attention)와 같은 다양한 **인지 관련 행동(cognitive-related behaviors)**을 포함하였다. 또한, 운동 과제(motor tasks), 복잡한 감정 처리 과제(emotional processing tasks), 삶의 만족도 평가 지표(life satisfaction measures) 등과 같은 **인지 비관련 행동(cognitive less-related behaviors)**도 포함시켰다. 이러한 행동 변수들을 통해, 인지 요인 점수 예측에 중요한 FC 엣지들이 인지 기능에 비해 운동이나 감정 기능을 덜 잘 예측하는지를 평가할 수 있다.

선택된 25개의 행동 지표는 다음의 10개 영역(domains)에 걸쳐 분포되어 있다:

1. **작업 기억(Working Memory)**:

   * WM 과제 2-back 조건의 중앙 반응 시간(Median Reaction Time of 2-back condition in Working Memory Task in fMRI scanner, WM Task 2bk Median RT)

2. **언어 능력(Language Ability)** (3개 지표):

   * 이야기 조건(Story condition)에서의 언어 과제 정확도(Language Task Story Accuracy)
   * 이야기 조건에서의 평균 난이도(Story Avg Difficulty)
   * 이야기 조건에서의 중앙 반응 시간(Language Task Story Median RT)

3. **지속적 주의(Sustained Attention)** (4개 지표):

   * Short Penn CPT에서의 학습률(SCPT LRNR)
   * 민감도(Sensitivity, SCPT SPEC)
   * 특이도(Specificity, SCPT SEN)
   * ‘True’ 반응의 중앙 반응 시간(Median Response Time for True, SCPT TPRT)

4. **공간 지남력(Spatial Orientation)** (3개 지표):

   * Penn Line Orientation Test의 정확한 반응 시간(Correct RT, VSPLOT CRTE)
   * 오프셋(Offset, VSPLOT OFF)
   * 총 완료율(Total Completion, VSPLOT TC)

5. **자기조절(Self-Regulation)**:

   * \$40,000 할인 선택의 면적 지표(Delay Discounting: Area Under the Curve for \$40K, DDisc AUC 40K)

6. **언어적 에피소드 기억(Verbal Episodic Memory)**:

   * Penn 단어 기억 검사에서 정답 반응의 중앙 반응 시간(Median RT for Correct Responses in Penn Word Memory Test, IWRD RTC)

7. **심리적 안녕(Psychological Well-being)**:

   * 주관적 삶의 만족도(Life Satisfy)

8. **사회적 관계(Social Relationship)** (4개 지표):

   * 지각된 대인 거절(Perceived Interpersonal Rejection, Rejection)
   * 외로움과 사회적 고립(Loneliness)
   * 타인으로부터 받은 도움 행동 인식(Instrumental Support, Instru Supp)
   * 지각된 스트레스 수준(PercStress)

9. **감정(Emotion)** (3개 지표):

   * 분노 감정의 강도(Anger Affect)
   * 슬픔 감정의 강도(Sadness)
   * 공포 감정의 강도(Fear Affect)

10. **운동(Motor)** (4개 지표):

    * 지구력(Endurance)
    * 악력(Grip Strength, Strength)
    * 보행 속도(Walking Speed, Gait Speed Component)
    * 손의 기민성(Dexterity)

각 행동 지표에 대한 세부 설명은 논문 **표 3**에 정리되어 있다. 모든 행동 점수는 예측 모델에 입력되기 전 **z-점수(z-score)**로 표준화되었다.

이들 25개 행동 지표 각각에 대해, 인지 요인 점수와의 관계 정도를 평가하기 위해 **스피어만 상관관계(Spearman correlation)**를 계산하였다. 이 상관계수를 우리는 ‘**인지 부하량(cognitive loading)**’이라 정의하였다. 인지 요인 점수와 통계적으로 유의미한 상관을 보인 행동들은 **인지 관련 행동(cognitive-related behaviors)**으로 간주되며, 그렇지 않은 행동들은 **인지 비관련 행동(cognitive less-related behaviors)**로 분류된다.

---

### 2.6 기능 연결성 기반 행동 예측 프레임워크

(Framework of FC based behavioral prediction)

우리는 인지 요인 점수(cognitive factor score) 예측에 유의미하게 기여한 기능 연결성 엣지(functional connectivity edges)가 운동(motor)이나 감정(emotion) 기능보다 인지 기능(cognitive functions)을 더 잘 나타낼 수 있을 것이라는 가설을 세웠다. 이를 검증하기 위해, 우리는 세 가지 비교 가능한 모델을 구축하고, 이들 모델이 행동 수행(behavior performance)을 예측하는 정확도(prediction accuracy)를 비교하였다.

세 모델은 동일한 교차검증(cross-validation) 전략을 사용하였으며, **특징 선택(feature selection)** 방식만 서로 달랐다.
첫 번째 모델인 **인지 온톨로지 기반 예측 모델(Cognitive Ontology based Prediction Model, COPM)**은 인지 요인 점수 예측에 있어 중요도가 높은 FC 엣지를 선택하였다. 구체적으로, 우리는 릿지 회귀(ridge regression)에서 도출된 절대 β 계수(absolute β coefficients)를 기준으로 상위 10% (총 7,980개)의 엣지를 선택하였다. COPM은 이후 이 엣지들만을 사용하여 다양한 행동을 예측하였으며, 예측 정확도는 100회 반복을 통해 평균되었다.

이와 비교하기 위한 **두 가지 베이스라인 모델(baseline models)**도 설정되었다:

* 첫 번째는 **전체 기능 연결성 모델(Full-FC, F-F)**로, 모든 FC 엣지를 이용하여 행동 점수를 예측하였다.
* 두 번째는 **릿지 회귀 기반 연결망 예측 모델(ridge-regression based Connectome Predictive Model, rCPM)**로, COPM과 동일한 수의 엣지(7,980개)를 사용하였다. 그러나 COPM이 인지 요인 점수 예측을 위해 FC 엣지를 선택하는 반면, rCPM은 **각 행동 예측에 특화된 FC 엣지**를 선택한다. 구체적으로는, 훈련 세트(training set) 내에서 해당 행동에 대한 회귀 계수의 절댓값을 기반으로 엣지를 정렬하고 상위 항목을 선택한다.

각 모델은 다음과 같은 방식으로 평가되었다.

* **스플릿-하프 검증(split-half validation)** 방식으로 데이터를 훈련 세트와 검증 세트로 나눈다.
* 각 반복마다 훈련-검증 역할을 바꾸며 두 번 수행된다.
* 피어슨 상관 계수(Pearson’s R)와 평균 제곱 오차(Mean Squared Error, MSE)를 통해 예측 정확도를 측정한다.
* 결과는 여러 반복을 통해 평균 처리된다.

마지막으로, 우리는 COPM이 인지 요인 점수와 관련된 행동(즉, **인지 부하량(cognitive loading)**이 높은 행동)을 더 잘 예측하는지 검증하고자 하였다. 이를 위해 다음을 수행하였다:

1. 앞서 정의된 25개 행동 각각에 대해 **원점수(raw performance)**와 인지 요인 점수 간의 상관관계(스피어만 상관계수)를 구하여 ‘**인지 부하량**’으로 정의하였다.

2. 각 모델의 예측 정확도와 인지 부하량 간의 상관관계를 계산하였다. 결과는 다음과 같이 명명하였다:

   * COPM-R: COPM 모델의 예측 정확도와 인지 부하량 간의 상관
   * F-F Model-R: F-F 모델의 상관
   * rCPM-R: rCPM 모델의 상관

3. COPM이 인지 요인과 밀접한 행동을 더 정확하게 예측하는지 확인하기 위해, **세 모델의 상관계수(COPM-R, F-F Model-R, rCPM-R)** 간 비교를 수행하였다. 이때 R의 **쌍차 상관 비교(correlated correlations comparison)**를 위해 **R의 cocor 함수(Diedenhofen and Musch, 2015; Silver et al., 2004)**를 사용하였다.

COPM-R이 F-F Model-R 및 rCPM-R보다 높다면, COPM이 인지와 밀접한 행동을 더 정확히 예측함을 의미한다.

또한, COPM의 이점이 **인지 관련 행동(cognitive-related behaviors)**에 국한된 것임을 보여주기 위해, 우리는 다음의 비교를 수행하였다:

* 인지 부하량이 높은 과제와 낮은 과제 그룹으로 나누고,
* 각 모델의 평균 예측 정확도를 **윌콕슨 부호 순위 검정(Wilcoxon signed-rank test)**을 통해 비교하였다.
* 모든 p-값은 **FDR(거짓 발견률) 보정(false discovery rate correction)**을 적용하였다.

한편, 일부 행동은 본질적으로 신뢰도가 낮아 정확히 예측되기 어렵다는 선행 연구(Gell et al., 2024)를 고려하여, COPM의 예측 정확도와 해당 행동의 **검사-재검사 신뢰도(test-retest reliability)** 간의 관계도 추가 분석하였다. 이를 위해:

* **46명의 참여자**가 수행한 25개 행동의 **검사-재검사 데이터셋(test-retest dataset)**을 사용하였다.
* 신뢰도는 **ICC(상관계수, intraclass correlation coefficient)**를 통해 측정되었으며,
* **Rex Toolbox(Xu et al., 2023)**로 계산되었다.
* 혼합효과 선형 모델(mixed-effects linear model)을 기반으로 하여, 세션과 피험자를 랜덤 효과(random effect)로 설정하였다.
* 최종적으로 각 행동의 ICC와 COPM 예측 정확도 간의 스피어만 상관관계를 계산하였다.

---

### 2.7 데이터셋 간 예측 안정성 평가

(Cross-dataset predictive efficiency of the COPM)

우리는 **COPM(Cognitive Ontology based Prediction Model)**이 인지 기능(cognitive functions)을 예측하는 능력을 **HCP-D 데이터셋**에서 평가하였다. 이 데이터셋은 HCP-YA와 유사한 행동 과제(behavioral tasks)를 포함하지만, 연령대가 **8세에서 22세** 사이의 아동 및 청소년에 초점이 맞추어져 있다. 우리의 가설은 다음과 같다:

> 만약 COPM이 HCP-D 데이터셋에서도 F-F 모델(Full-FC model)과 rCPM(ridge-regression based Connectome Predictive Model)보다 **인지 기능 예측**에서 우수한 성능을 보이되, **운동(motor)** 및 **감정(emotion)** 기능에서는 세 모델 간 성능 차이가 없을 경우, 이는 인간 인지를 나타내는 **안정적인 FC 엣지 집합(stable set of functional connectivity edges)**이 존재함을 시사한다.

이를 검증하기 위해 우리는 총 **8개의 행동 과제**를 선택하였으며, 이는 다음과 같이 분류된다:

* **인지 관련 기능(cognitive-related functions)** 측정 과제 (총 6개):

  * 실행 기능(executive function) 평가:

    * Dimensional Card Sorting
    * Flanker test
    * List Sorting Working Memory
    * Picture Sequence Memory
  * 언어 능력(language ability) 평가:

    * Oral Reading Recognition Test
    * Picture Vocabulary Test

* **인지 비관련 기능(cognitive less-related functions)** 평가 과제 (총 2개):

  * 운동 기능(motor ability):

    * Grip Strength
  * 감정 처리(emotional processing):

    * Fear Affect

이 과제들의 세부 설명은 **보조표 S2(S2 Table)**에 수록되어 있다.

우리는 HCP-D 데이터셋에서 이 8개 행동을 예측하기 위해 COPM, F-F 모델, rCPM을 동일한 절차로 적용하였다. 이때, HCP-YA 데이터셋에서 인지 요인 점수 예측에 기여한 **상위 10% FC 엣지(7980개)**를 그대로 사용하였으며, HCP-D 데이터셋 내에서 인지 요인을 새롭게 재구성하지 않았다. 즉, 이 분석은 HCP-YA에서 도출된 FC 엣지들의 **데이터셋 간 예측 안정성(cross-dataset predictive stability)**을 직접 평가하는 방식이었다.

우리는 두 종류의 행동(인지 관련 vs. 인지 비관련)에 대한 예측 정확도를 세 모델 간 비교하였다. 분석 결과는 다음과 같았다:

* COPM은 **인지 관련 기능** 과제에 대해 **인지 비관련 기능** 과제보다 **유의미하게 더 높은 예측 정확도**를 보였다 (p < 0.001, **윌콕슨 효과 크기 Wilcoxon effect size**, r = 0.868).
* 인지 관련 기능 과제 6개 중, **5개 과제에서 COPM이 F-F 모델과 rCPM 모두보다 더 높은 예측 성능**을 보였다 (p < 0.05, **FDR 보정** 적용; Fig. 5 및 Table 5 참조).
* 반면, 인지 비관련 기능 과제 2개에 대해서는 COPM, F-F 모델, rCPM 간 예측 정확도 차이가 유의하지 않았다 (p > 0.05, FDR 보정).

---

### 2.8 COPM에서 사용된 기능 연결성(FC) 엣지의 가변성, 백질 구조 기반, 유전적 기반 탐색

(Exploring the FC variability, white matter structural basis, and genetic basis of FC edges in COPM)

COPM(Cognitive Ontology based Prediction Model)에서 사용된 **7,980개 기능 연결성 엣지(FC edges)**의 생물학적 기반을 탐색하기 위해, 우리는 다음 세 가지 생물학적 지표에 대한 관계를 분석하였다:

1. **기능 연결성 가변성(functional connectivity variability)**
2. **백질 구조 연결성(white matter structural connectivity)**
3. **유전자 발현 유사도(gene expression similarity) 패턴**

이 분석은 Yang et al. (2023)의 방법론을 기반으로 수행되었다.

먼저, 우리는 인지 요인 예측 모델에서 각 엣지가 기여한 정도를 나타내는 **선형 기여 가중치(linear contribution weight)**를 계산하였다. 이를 통해 400 × 400 크기의 다음 네 개 행렬(matrix)을 생성하였다:

* 기여 가중치 행렬(contribution weight matrix)
* 기능 연결성 강도 가변성(FC strength variability)
* 백질 구조 연결성(strength of structural connectivity, SC)
* 유전자 발현 유사도(gene expression similarity)

우리는 **Schaefer 400 영역 분할(Schaefer parcellation, Schaefer et al., 2018)**을 기반으로 하여 이 네 가지 지표를 각 네트워크 단위로 요약하였다. Schaefer atlas의 400개 parcel은 **Yeo 17 네트워크(Yeo et al., 2011)**로 분류될 수 있으며, 각 지표를 네트워크 간 연결(internetwork)과 네트워크 내 연결(intranetwork)로 나누어 평균을 구하였다. 이로써 각 행렬은 17 × 17 크기의 네트워크 간 행렬로 변환되었다.

다음으로, 우리는 기여 가중치 행렬과 나머지 세 지표(FC 가변성, SC, 유전자 발현 유사도) 간의 **스피어만 상관관계(Spearman correlation)**를 계산하였다.

통계적 유의성을 평가하기 위해, 우리는 **퍼뮤테이션 테스트(permutation test)**를 수행하였다. 구체적으로, 400 × 400 전체 FC 행렬에서 무작위로 7,980개의 엣지를 10,000회 샘플링하였고, 각 샘플에 대해 17 × 17 평균 네트워크 행렬을 생성하였다. 그 후, 실제 기여 가중치 행렬과 퍼뮤테이션으로 생성된 행렬 간의 상관계수를 비교하였다.

**유의 수준(p-value)**은 실제 상관계수가 퍼뮤테이션에서 얻어진 상관계수 분포를 얼마나 초과했는지로 정의하였으며, **보정된 유의 수준**은 p < 0.05/3 (다중 비교 보정) 기준을 적용하였다.

---

### 2.9 다양한 엣지 선택 비율 및 분할 방식에 따른 검증 분석

(Validation analysis across varied edge selection percentiles and parcellation scheme)

우리의 주요 결과의 안정성(stability)을 평가하기 위해, 우리는 인지 요인 점수(cognitive factor score)를 예측하는 데 가장 큰 기여를 한 엣지(edges)를 **다양한 선택 비율(thresholds)**에서 분석하였다:

* 상위 20%
* 상위 30%

각 임계값(threshold)마다, 우리는 기여도가 가장 높은 엣지들을 선택하고, 초기 분석 절차를 반복하였다. 이 과정에는 다음이 포함된다:

* 특정 행동 과제(task-specific behaviors)에 대한 예측 수행
* 각 임계값에서 **인지 부하량(cognitive loading)**과 **예측 정확도(prediction accuracy)** 간의 상관관계 분석

분석 결과, 우리는 모든 임계값(20%, 30%)에서 유의미한 상관관계를 일관되게 관측하였다:

* 20%: r = 0.57, p = 0.002
* 30%: r = 0.51, p = 0.005

이러한 결과는 인지 요인과 높은 상관을 가지는 행동일수록 예측 정확도가 높다는 초기 결과를 강화하며, 다양한 임계값에서도 **인지 관련 기능(cognitive-related functions)**을 안정적으로 반영함을 시사한다.

우리는 또한 **rCPM(ridge-regression based Connectome Predictive Model)**을 동일한 방식으로 분석하였다. rCPM은 COPM과 동일한 수의 엣지를 사용하되, 각 행동 예측에 특화된 엣지를 선택한다.

* rCPM에서도 인지 부하량과 예측 정확도 간의 상관관계는 유의미하였다:

  * 20%: r = 0.46, p = 0.02
  * 30%: r = 0.46, p = 0.02

하지만, 두 모델 간 상관관계를 직접 비교해보면 COPM이 더 높은 상관을 보였다:

* 20%: z = 2.50, p = 0.01
* 30%: z = 2.27, p = 0.02

이 결과는 **엣지 선택 비율이 다소 늘어나더라도 COPM이 여전히 인지 기능 표현에 특화된 엣지를 효과적으로 포착**함을 보여준다. 특히 COPM은 **더 적은 수의 기능 연결성 엣지를 사용하여 인지 요인과 관련된 행동을 더 정확히 예측**할 수 있음을 시사한다.

마지막으로, 우리는 COPM의 견고성(robustness)을 추가로 확인하기 위해 **다른 뇌 분할 방식(brain parcellation scheme)**을 사용하였다.

* 기존에는 **Schaefer atlas** (400 영역)를 사용하였으나,
* 이번에는 **Glasser atlas (Glasser et al., 2016)**를 사용하여 360 × 360 기능 연결망을 구축하였다.

이 실험에서는 계산 비용 문제로 rCPM을 생략하고, **F-F 모델만 베이스라인으로 사용**하였다.
COPM과 F-F 모델을 Glasser atlas 기반으로 비교 분석한 결과, 주요 분석 결과가 재현되었으며, 이는 COPM 모델의 일반성과 견고성을 입증한다.

---

## 3. 결과 (Results)

### 3.1 인지 요인 점수 예측에 기여하는 핵심 연결망 식별

(Identifying core connectomes contributing to cognitive factor score prediction)

우리는 인지 요인 점수(cognitive factor score)를 예측하기 위해 릿지 회귀(ridge regression)를 적용하였으며, 그 결과 상위 10%에 해당하는 총 **7,980개의 기능 연결성 엣지(functional connectivity edges)**를 추출하였다. 이 엣지들은 다음과 같은 두 가지 방식으로 도출되었다:

1. **회귀 가중치 기반 절대값 기준**
2. **Haufe 변환(Haufe transform)**을 통한 계수 기반

흥미롭게도, 두 방법 모두에서 **동일한 17개 네트워크(Yeo 17 network)** 내의 엣지들이 높은 중요도를 보였다 (예: 전두두정망(frontoparietal network), 배측주의망(dorsal attention network), 기본모드망(default mode network) 등).

다음은 주된 결과 요약이다:

* 상위 엣지들의 연결은 **고등연합피질(higher-order association cortex)**에 집중되어 있었다.
* 반면, **일차 감각(sensory)** 또는 **운동 피질(motor cortex)**에서의 엣지는 드물었다.

기능 연결 엣지의 기여도를 네트워크 수준에서 평균 낸 결과, **FPN(전두두정망), DMN(기본모드망), DAN(배측주의망)** 내 엣지가 인지 요인 점수 예측에 가장 크게 기여하는 것으로 나타났다 (Fig. 2a 참조).

또한, COPM(Cognitive Ontology based Prediction Model) 기반 엣지들의 공간적 분포는 다음과 같은 뚜렷한 특성을 보였다:

* 네트워크 간 연결(internetwork connectivity)이 네트워크 내 연결(intranetwork)보다 훨씬 높은 비율을 차지함
* 이는 다양한 인지 영역(cognitive domains)에서의 정보 통합 및 분산 처리(integration and distributed processing)를 뒷받침하는 구조로 해석될 수 있음

### Haufe 변환 결과

Haufe 변환을 적용한 결과 역시 유사한 공간적 분포를 보였으며, 특히 다음 네트워크 간 연결에서 강한 기여도를 나타냈다:

* **전두두정망(FPN)** – **기본모드망(DMN)**
* **기본모드망(DMN)** – **배측주의망(DAN)**
* **전두두정망(FPN)** – **배측주의망(DAN)**

이는 **FPN, DAN, DMN**이 인간의 고차원 인지(high-order cognition)를 위한 핵심 연결망(core connectomes)으로 기능함을 시사한다.

이러한 결과는 400개 피질 영역(Schaefer atlas 기준) 또는 17개 네트워크 수준(Yeo atlas 기준) 모두에서 일관되게 관찰되었으며, **인지 기능의 예측에 특화된 연결망이 존재한다는 실증적 증거(empirical evidence)**를 제공한다.

---

### 3.2 COPM은 인지 기능과 높은 관련을 갖는 행동을 더 잘 예측한다

(COPM better predicts behaviors highly associated with cognitive functions)

우리는 COPM(Cognitive Ontology based Prediction Model)의 유효성을 평가하기 위해, 총 25개의 행동 변수(behavioral variables)에 대해 예측 정확도(prediction accuracy)를 측정하였다. 이들 행동 변수는 **인지 기능과의 관련성(cognitive association)** 수준이 서로 다른 항목들로 구성되어 있었다.

각 행동 변수에 대해 다음과 같은 지표를 분석하였다:

1. **실제 행동 점수와 인지 요인 점수 간의 스피어만 상관관계(Spearman correlation)** → “**인지 부하량(cognitive loading)**”이라 정의
2. **COPM, F-F 모델(Full-FC), rCPM 모델**의 예측 정확도
3. **각 모델의 예측 정확도와 인지 부하량 간의 상관관계**

#### 결과 요약:

* COPM은 **인지 부하량이 높은 행동일수록 더 정확하게 예측**하였다 (r = 0.63, p < 0.001; Fig. 3b).
* 반면, F-F 모델(r = 0.31, p = 0.13)과 rCPM(r = 0.35, p = 0.08)은 이러한 경향이 약하거나 유의하지 않았다.

세 모델 간 상관관계를 직접 비교한 결과, **COPM이 F-F 및 rCPM보다 유의하게 더 높은 상관을 보였다** (cocor 패키지 기반 z-검정 결과):

* COPM vs. F-F: z = 2.60, p = 0.009
* COPM vs. rCPM: z = 2.14, p = 0.03

또한, 우리는 행동 변수를 **인지 부하량 상위 13개(인지 관련)**와 **하위 12개(인지 비관련)**로 나누어 모델별 예측 정확도를 비교하였다:

* COPM은 인지 관련 행동에서 **F-F 모델(p = 0.02)** 및 **rCPM(p = 0.02)**보다 유의하게 더 높은 예측 성능을 보였다 (Wilcoxon signed-rank test, FDR 보정 포함).
* 그러나 인지 비관련 행동에서는 세 모델 간 유의한 차이가 없었다 (p > 0.1; Fig. 3c 참조).

이 결과는 **COPM이 인지 요인과 밀접한 행동을 더 효과적으로 포착하며, 그 설계 목적과 일치하는 정밀한 예측 특성을 가진 모델**임을 시사한다.

#### 신뢰도와의 관계 분석:

COPM의 예측 정확도가 단지 **행동의 측정 신뢰도(test-retest reliability)**를 반영한 결과가 아님을 검증하기 위해, 우리는 **검사-재검사 신뢰도(intraclass correlation coefficient, ICC)**와 예측 정확도 간의 상관관계를 분석하였다.

* 결과: r = 0.34, p = 0.09 → 통계적으로 유의하지 않음
* 이는 COPM의 예측 정확도가 **단순히 신뢰도가 높은 항목에서만 잘 작동하는 것이 아님**을 시사한다 (즉, **모델의 진정한 선택성**을 의미).

---

### 3.3 COPM은 아동-청소년 데이터셋(HCP-D)에서도 인지 기능 예측에서 뛰어난 성능을 보인다

(COPM performs well in predicting cognitive functions in the HCP-D dataset)

우리는 **HCP-D 데이터셋**(아동 및 청소년 대상)을 사용하여 COPM(Cognitive Ontology based Prediction Model)의 **일반화 가능성(generalizability)**과 **예측 안정성(predictive stability)**을 평가하였다.

이때, **HCP-YA**에서 도출된 7,980개의 기능 연결성 엣지(FC edges)를 그대로 적용하였으며, 새로운 인지 요인 점수를 학습하거나 재추정하지 않았다. 즉, **FC 엣지 집합의 이식성(transferability)**을 검증하였다.

#### 결과 요약:

* **인지 관련 행동(6개)**에 대해 COPM은 **F-F 모델(Full-FC)** 및 **rCPM**보다 일관되게 높은 예측 정확도(Pearson’s R)를 보였다 (Fig. 5a).

  * COPM의 평균 예측 정확도: R = 0.35
  * F-F 모델: R = 0.23
  * rCPM: R = 0.21

* 통계적으로도 COPM은 인지 관련 행동 예측에서 **두 베이스라인 모델보다 유의하게 우수**하였다:

  * COPM vs. F-F: p = 0.015
  * COPM vs. rCPM: p = 0.023
    (Wilcoxon signed-rank test, FDR 보정)

* **인지 비관련 행동(2개)**에 대해서는 세 모델 간 예측 정확도에 유의한 차이가 없었다 (p > 0.1; Fig. 5b).

* 추가적으로, 인지 관련 행동에서 COPM의 예측 정확도는 **인지 부하량(cognitive loading)**과 강한 상관관계를 보였다:

  * r = 0.84, p = 0.009
    → 이는 COPM이 인지 기능에 특화된 연결망을 기반으로 동작함을 다시 한번 입증

* 반면, F-F 및 rCPM은 이러한 경향을 보이지 않았다:

  * F-F: r = 0.30, p = 0.51
  * rCPM: r = 0.42, p = 0.33

이러한 결과는 COPM이 단지 특정 연령 집단에서만 작동하는 모델이 아니라, **발달기 인지 기능의 핵심 기반(core substrate)**을 잘 포착하고 있음을 시사한다.

---

### 3.4 COPM 엣지는 높은 기능적 가변성, 백질 연결성, 유전자 발현 유사성과 관련된다

(COPM edges relate to high functional variability, structural connectivity, and gene co-expression)

우리는 COPM(Cognitive Ontology based Prediction Model)에서 선택된 기능 연결성 엣지(FC edges)가 생물학적으로 의미 있는 특성을 갖는지를 확인하기 위해 다음 세 가지 분석을 수행하였다:

#### 1. 기능 연결성 가변성 (Functional Connectivity Variability)

* 기여 가중치(contribution weight)가 높은 엣지일수록 기능 연결성의 개인 간 변동성(individual variability in FC strength)이 크다는 것을 발견하였다.
* 상관계수: **r = 0.55, p < 0.001**
* 이는 인지에 중요한 FC 엣지가 **개인마다 크게 다르며** 개별 차이를 설명할 수 있는 정보(informative individual differences)를 담고 있음을 시사한다.

#### 2. 백질 구조 연결성 (Structural Connectivity, SC)

* FC 기여 가중치와 백질 기반 연결 강도(structural connection strength) 간에도 유의한 상관관계가 있었다.
* 상관계수: **r = 0.48, p < 0.001**
* 이는 인지 예측에 중요한 FC 엣지들이 백질 경로(white matter tracts)와 구조적으로 연결되어 있음을 의미한다.

#### 3. 유전자 발현 유사도 (Gene Co-expression Similarity)

* FC 기여 가중치와 유전자 발현 유사도(gene expression similarity) 간에도 강한 양의 상관관계가 확인되었다.
* 상관계수: **r = 0.51, p < 0.001**
* 이로써 COPM이 사용하는 엣지들이 동일하거나 유사한 유전자 발현 프로파일을 공유하는 뇌 영역 간 연결이라는 점이 밝혀졌다.

#### 통계적 유의성 평가 (Permutation Testing)

위의 결과들은 모두 **퍼뮤테이션 검정(permutation test)**을 통해 유의미함이 검증되었다. 10,000회 반복된 랜덤 샘플과 비교했을 때:

* 모든 결과가 **유의 수준 p < 0.001**을 만족하였고,
* 이는 COPM이 단지 통계적으로 의미 있는 것이 아니라, **기능적, 구조적, 분자생물학적으로도 의미 있는 뇌 연결망(core connectome)**을 구성함을 나타낸다.

---

요약하자면, COPM에서 식별된 기능 연결 엣지는 다음과 같은 특징을 가진다:

* 개인마다 강도 차이가 크며 (개인차 포착)
* 실제 뇌 백질 경로와 연결되고 (구조 기반)
* 유전적으로 유사한 유전자 발현 패턴을 보인다 (분자 기반)

이러한 결과는 **인지 기능을 예측하는 핵심 연결망(core connectome for cognition)**이 기능적·구조적·유전적 특이성을 동시에 지닌다는 사실을 뒷받침한다.

---

### 3.5 다양한 임계값과 분할 방식에서도 COPM의 핵심 연결망은 안정적으로 재현된다

(COPM connectomes are robust across thresholds and parcellation schemes)

우리는 COPM(Cognitive Ontology based Prediction Model)이 선택하는 핵심 기능 연결성 엣지(core FC edges)가 다음의 조건에서도 안정적으로 재현되는지를 확인하였다:

1. **엣지 선택 비율(edge selection percentile)** 변화
2. **뇌 분할 방식(brain parcellation scheme)** 변경

#### 1. 엣지 선택 비율 변화 (10%, 20%, 30%)

* 우리는 COPM의 기여 가중치(contribution weight)에 따라 상위 10%, 20%, 30% 엣지를 각각 선택하고, 네트워크 수준에서 연결 강도(distribution of edge weights)를 분석하였다.
* 결과:

  * 상위 엣지는 **전두두정망(FPN)**, **기본모드망(DMN)**, **배측주의망(DAN)**에 집중되었으며,
  * 네트워크 간 연결(internetwork connections)이 네트워크 내 연결(intranetwork)보다 일관되게 많았다 (Fig. S2, S3 참조).
  * 이는 엣지 선택 비율이 달라져도 COPM이 **고차 인지(higher-order cognition)**에 특화된 연결망을 안정적으로 포착함을 의미한다.

#### 2. 뇌 분할 방식 변경 (Schaefer 400 → Glasser 360)

* 기존 분석은 **Schaefer 400 파셀(atlas)** 기반이었으며, 이번에는 **Glasser 360 파셀**로 변경하여 동일한 절차를 수행하였다.
* 결과:

  * 예측 정확도와 인지 부하량(cognitive loading) 간의 상관관계가 여전히 유의미하였다 (r = 0.66, p = 0.002; Fig. S4).
  * 전두두정망, 기본모드망, 배측주의망 중심의 연결망 구성은 그대로 재현되었다.
* 결론: **분할 체계의 변화에도 불구하고 COPM의 핵심 연결망 구조는 견고하게 유지**된다.

이러한 결과는 COPM이 특정 조건에 과적합(overfitting)된 모델이 아니라, **보편적 인지 기능(cognitive functions)의 핵심 연결 구조를 포착**하고 있음을 시사한다.

---

## 4. 논의 (Discussion)

본 연구는 **인지 온톨로지 기반 머신러닝 접근법(ontology-guided machine learning approach)**을 통해, 다양한 인지 기능(cognitive functions)의 공통된 뇌 기반(common neural substrates)을 이해하고자 한 시도였다. 우리는 이 접근법을 통해 식별된 **핵심 기능 연결망(core functional connectome)**이 인지에 특화되어 있으며, 기능적, 구조적, 유전적 측면에서 모두 신경생물학적 기반(neurobiological basis)을 지닌다는 실증적 증거를 제시하였다.

### 주요 발견 요약:

1. **인지 기능 예측에 특화된 FC 엣지 집합**

   * 전두두정망(FPN), 기본모드망(DMN), 배측주의망(DAN)을 중심으로 구성됨
   * 다양한 인지 과제에서 전통적 모델보다 더 높은 예측 정확도 달성

2. **인지 부하량(cognitive loading)과 예측 정확도 간의 강한 정적 상관**

   * COPM은 인지 기능과 높은 관련성을 지닌 행동에서 가장 강력한 성능 발휘

3. **모델 이식성 및 일반화 가능성**

   * 청년 성인(HCP-YA)에서 훈련된 모델이 아동-청소년(HCP-D)에게도 유의한 성능을 보임

4. **신경생물학적 기반**

   * 높은 기능 연결 가변성(functional variability)
   * 강한 백질 구조 연결성(structural connectivity)
   * 높은 유전자 발현 유사도(gene co-expression similarity)

---

### 4.1 인간 인지의 핵심 연결망(Core Connectome of Cognition)

우리의 분석은 인지 기능 전반을 지탱하는 **공통된 기능 연결망(domain-general FC network)**의 존재를 강조한다.

* 이는 ‘기본적 작업 네트워크(core working networks)’ 또는 ‘범인지 네트워크(domain-general networks)’ 개념과 일치하며,
* 특히 **FPN, DAN, DMN 간의 상호작용**은 실행 기능(executive function), 주의(attention), 내적 사고(internal thought) 등 고차 인지에 필수적임이 거듭 입증되었다.

흥미롭게도, 이들 연결망은 다음과 같은 이론적 모델들과도 일치한다:

* **역동적 조절 이론(dynamic control hypothesis)**: FPN은 DMN과 DAN 사이의 전환 조절 허브로 작용
* **기능적 통합 모델(functional integration)**: 인지는 독립적 모듈의 총합이 아닌, **네트워크 간 통합적 처리(integrated network processing)**의 결과임

---

### 4.2 인지와 감각/운동/감정 기능의 분리

COPM은 인지 기능과 높은 관련성을 지닌 행동만을 안정적으로 예측하였으며, 감각(sensory), 운동(motor), 감정(emotional) 기능에 대해서는 예측력이 제한적이었다. 이는 다음을 시사한다:

* 인지 기능을 매개하는 연결망은 감각/운동/감정 처리에 관여하는 네트워크와 **부분적으로 독립적**임
* 이는 뇌가 기능적으로 분화(functionally segregated)되어 있다는 기존 신경과학 이론과 부합

---

### 4.3 인지 기능 연결망의 신경생물학적 기반

COPM에서 선택된 엣지들이 기능적·구조적·유전적으로도 유의미함은 중요한 발견이다.

* **기능 연결 가변성(functional variability)**:
  높은 변동성은 해당 엣지가 개인차(individual differences)를 잘 설명할 수 있음을 의미

* **백질 구조 연결성(structural connectivity)**:
  FC 엣지가 실제 백질 경로(tracts)를 통해 해부학적으로 연결되어 있음을 시사

* **유전자 발현(gene expression)**:
  해당 뇌 영역들이 유사한 유전자 발현 프로파일을 공유하며, 이는 기능적 연계성을 유도하는 생물학적 기반이 될 수 있음

---

### 4.4 방법론적 공헌

* 우리는 **인지 온톨로지(cognitive ontology)** 기반 머신러닝 접근법을 통해, 다수의 인지 과제에서 공통적인 신경 지표를 추출함
* 이는 기존의 개별 과제 기반 모델(single-task models)이나 행동별 예측 모델들보다 일반성과 해석 가능성 측면에서 우수함

---

## 5. 결론 (Conclusion)

본 연구는 인간 인지(human cognition)를 이해하고 예측하기 위한 새로운 접근법으로서, **인지 온톨로지 기반 예측 모델(COPM: Cognitive Ontology-based Predictive Model)**을 제안하고 실증적으로 검증하였다.

### 주요 결론은 다음과 같다:

1. **COPM은 다양한 인지 기능(cognitive functions)에 공통적으로 작용하는 핵심 기능 연결망(core functional connectome)을 식별**한다.

   * 이 연결망은 전두두정망(frontoparietal network), 기본모드망(default mode network), 배측주의망(dorsal attention network) 등 고차 인지에 핵심적인 네트워크 간의 상호작용으로 구성되어 있다.

2. COPM은 인지 기능과 높은 관련이 있는 행동 지표들에 대해 **기존 모델보다 높은 예측 정확도(predictive accuracy)**를 보인다.

   * 예측 성능은 인지 부하량(cognitive loading)에 비례하여 증가하였다.

3. COPM은 **발달기 인구(아동·청소년)의 독립적 데이터셋(HCP-D)**에서도 높은 성능을 재현하였으며,

   * 이는 본 모델이 특정 연령 집단에 국한되지 않고 **범용적 인지 기반(generalizable cognitive substrates)**을 포착하고 있음을 시사한다.

4. COPM이 선택한 기능 연결 엣지는 다음의 **신경생물학적 기반(neurobiological underpinnings)**과 강한 관련을 가진다:

   * 높은 기능 연결 가변성(functional variability)
   * 강한 백질 구조 연결성(structural connectivity)
   * 유사한 유전자 발현 패턴(gene co-expression similarity)

---

### 결론적으로, 본 연구는:

* **인지 과제들의 구조적 관계(cognitive ontology)**를 활용하여
* **공통된 뇌 기반(common brain basis)**을 밝혀내고
* **개별 행동 및 인지 기능 예측에 효과적인 기능 연결성 모델**을 제시함으로써

**인간 인지의 신경기반(neural architecture of human cognition)을 규명하고자 하는 신경과학·인지과학·기계학습 분야에 의미 있는 기여**를 하였다.

---
