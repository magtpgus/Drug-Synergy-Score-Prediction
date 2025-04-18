# Drug-Synergy-Score-Prediction

🧬 Multi-Omics를 활용한 Drug Synergy Prediction 

이 프로젝트는 다양한 오믹스 데이터(CNV, methylation, mutation, expression)를 통합하여, 약물 조합에 대한 반응 (Synergy Score) 을 예측하는 Graph Neural Network 모델입니다. 
DGL과 PyTorch 프레임워크를 사용하여 유전자-약물 간의 복합 그래프를 구성하고, 약물 조합의 치료 효과를 정량적으로 예측합니다.

---

📌 프로젝트 개요

- 주제: Multi-omics 데이터를 활용한 약물 시너지 예측
- 모델: Graph Neural Network
- 데이터:
  - `cnv_refactored.tsv`: Copy Number Variation
  - `methylation_refactored.tsv`: Methylation
  - `mutation_refactored.tsv`: Mutation
  - `expression_refactored.tsv`: Gene Expression
  
---

🧠 주요 특징

1. 데이터 통합 및 전처리
- 각 오믹스 데이터는 `load_omics_data()`를 통해 개별적으로 불러오며,
- 세포주(GDSC 기준) 별 feature로 구성됩니다.

2. Graph Construction
- 유전자-약물 구조의 이종 그래프를 생성
- GNN을 통해 각 노드 간 관계를 학습하고 시너지 예측에 활용

---

📊 예측

- 약물 조합 간 Synergy Score
- Pearson Correlation Coefficient(PCC)를 주요 성능 지표로 활용

---

🚀 실행 환경

- Python 3.8+
- 주요 패키지: `torch`, `dgl`, `pandas`, `numpy`, `sklearn`
