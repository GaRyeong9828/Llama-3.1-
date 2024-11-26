<a name = "title"></a>
# Llama 3.1 문서 요약 기능 테스트
---
<a name = "author"></a>
작성자 : 경북대학교 전자공학부 인공지능전공/2024003120/이가령
---

<a name = "purpose"></a>
# 1. 목적

본 작성자는 Llama 3.1의 문서 요약 기능이 얼마나 효과적이고 신뢰할 수 있는지를 평가하기 위해 이 테스트를 진행했다.

---
<a name = "license"></a>
# 2. LLaMA 3 License
>[LLaMA 3 깃허브 LICENSE 문서](https://github.com/meta-llama/llama3/blob/main/LICENSE)

---

<a name = "caution"></a>
# 3. 주의사항
본 게시글은 대학교 1학년 학생이 과제를 수행하며 AI를 활용한 경험을 바탕으로 작성된 내용입니다. 작성자는 해당 분야의 전문가가 아니며, 내용에 오류가 있을 수 있습니다. 참고 자료로만 활용하시기를 권장합니다.

<a name = "chapter"></a>
# 4. 목차
>### <a href = "#title">제목</a></br>
>#### <a href = "#author">작성자</a>
>### 1. <a href = "#purpose">목적</a>
>### 2. <a href = "#license">LLaMA 3 라이선스</a>
>### 3. <a href = "#caution">주의사항</a>
>### 4. <a href = "#chapter">목차</a>
>### 5. <a href = "#test">테스트</a>
>>#### 1. <a href = "#preparation">테스트 준비</a>
>>#### 2. <a href = "#procedure">테스트 절차</a>
>>#### 3. <a href = "#analyze">결과 분석</a>
>>#### 4. <a href = "#result">결론</a>
>### 6. <a href = "#pros_and_cons">장점&단점</a>
>### 7. <a href = "#feedback">피드백</a>

---
<a name = "test"></a>
# 5. 테스트
<a name = "preparation"></a>
## 1. 테스트 준비

### 문서 수집
다양한 주제와 길이의 문서를 선정하여 테스트 대상 문서로 사용했습니다. 총 10개의 문서를 선정하여 다양한 시나리오를 반영했다.

### 요구 사항 정의
문서 요약의 요구 사항을 설정했습니다. 예를 들어, 요약의 길이, 특정 정보 포함 여부(예: 키워드 강조) 등을 미리 정했다.

### Llama 3.1 사용방법 찾기
실제로 Github의 Llama3 프로젝트에 있는 Llama3.1을 안내된 절차에 따라 다운로드 받아 테스트를 할 수 있다면 가장 좋다. 하지만 방법도 어려울 뿐더러 UI도 복잡하다. 또한 보통 가정에서 사용하는 컴퓨터로는 모델의 크기가 큰 Llama 3.1을 돌리기에는 사양이 적절하지 않다. 따라서 작성자는 해당 테스트에서 UI도 간편하고 집의 컴퓨터 사양으로도 Llama3.1을 사용할 수 있는 Msty에서 테스트를 진행하였다.

<a name = "prodcedure"></a>
## 2. 테스트 절차

### Llama 3.1 모델 설정
Msty에서 Meta Llama를 다운받아 Llama 3.1을 설치하여 문서 요약 기능을 사용할 수 있도록 설정했다. Llama 3.1은 8B, 70B, 405B를 지원하고 있다. 나는 8B모델을 사용했다.

### 입력 데이터 전송
신뢰할 수 있는 사이트에서 수집한 문서를 모델에 입력하여 요약 결과를 요청했다. 한글 문서의 경우, DeepL에서 문서를 영어로 변환한 후 Llama 3.1이 출력한 요약문을 다시 DeepL을 통해 한글 문서로 변환하였다.

### 결과 수집
모델로부터 반환된 요약 결과를 수집하고, 원래 문서와 비교하여 분석했다.

### 결과물

1. 영어 뉴스
![질문](https://github.com/user-attachments/assets/c0cad542-742e-43d3-b5c2-55e738f9dde3)
출처 : By Deidre McPhillips/"Free Covid-19 tests are available again. Here’s how to get them"/CNN/2024,09.26
![답변](https://github.com/user-attachments/assets/338f6d64-bee0-4752-a2f6-37714db7e585)

2. 영어 논문
![image](https://github.com/user-attachments/assets/dfab6cf8-76b7-45e8-8e49-b978eebc51c9)
출처 : Li Yang, Shasha Liu, Jinyan Liu, Zhixin Zhang, Xiaochun Wan, Bo Huang, Youhai Chen & Yi Zhang/"COVID-19: immunopathogenesis and Immunotherapeutics"/Signal Transduction and Targeted Therapy/ 5, Article number: 128 (2020)/p.2
![image](https://github.com/user-attachments/assets/841e07ef-2d39-47c3-b940-286aae0e0774)

3. 한국어 뉴스
![image](https://github.com/user-attachments/assets/40b472e5-bff9-4882-ae05-01fb940870f7)
출처 : 내 손안에 서울/"황홀한 가을밤…서울세계불꽃축제! 교통통제 구간은?"/내 손안에 서울/2024.10.02
![image](https://github.com/user-attachments/assets/fd358620-f029-4c17-886d-5e8e988dda9f)

4. 한국어 논문
![image](https://github.com/user-attachments/assets/8c386679-c24c-47db-b003-42c036201f48)
출처 : 황응수,박정규, 차창용/"바이러스 감염에 대한 면역반응"/대한면역학회/2004년/p.74
![image](https://github.com/user-attachments/assets/40579734-a9db-4e49-91ef-b7c92ff62637)

<a name = "analyze"></a>
## 3. 결과 분석

### 정확도 및 관련성
요약 결과의 정확도와 원래 문서에서 중요한 정보가 잘 반영되었는지를 평가했다. 대부분의 요약이 주제를 정확히 반영하고 있음을 확인했다.

### 요약 길이 및 형식
테스트의 요구 사항에 맞춰 적정 길이로 요약된 경우가 많아 비즈니스 환경에서도 유용할 것으로 판단했다.

<a nmae = "result"></a>
## 4. 결론

Llama 3.1의 문서 요약 기능은 효과적으로 문서를 간결하게 요약할 수 있음을 확인했다. 그러나 특정 분야에 대한 전문 용어와 지식이 포함된 문서에서는 다소 부족한 성능을 보였다. 한국어 기능도 지원은 하나 영어로 된 문서와 비교했을 때는 다소 부족한 성능을 보였다. 그러나 강력한 성능과 다국어 지원, 자유로운 변형 가능성을 제공하는 점에서 높게 평가할 수 있다.

---

<a name = "pros_and_cons"></a>
# 6. 장단점
 위의 테스트를 통해 발견한 Llama 3.1의 문서 요약 기능의 장점과 단점을 정리해보았다.
### 장점
+	**빠른 요약 생성** : Llama 3.1은 대량의 정보를 빠르게 요약할 수 있어, 사용자가 핵심 내용을 신속하게 파악할 수 있도록 도와줍니다.
+	**높은 정보 유지율** : 문서의 중요한 세부 사항과 맥락을 잘 유지하면서 요약을 생성하여, 사용자가 전체 내용을 놓치지 않도록 합니다.
+	**다양한 스타일의 요약** : 여러 형식(예: 리스트, 문장 기반)으로 요약할 수 있는 기능이 있어, 사용자 요구에 맞춰 조정할 수 있습니다.
+	**사용자 친화적 인터페이스** : 사용자가 요약 기능을 쉽게 사용할 수 있도록 설계되어, 기술적인 배경이 없는 사용자도 편리하게 이용할 수 있습니다.

### 단점
+	**맥락 손실 가능성** : 때때로 문서의 복잡한 맥락이나 뉘앙스를 완전히 반영하지 못하는 경우가 있으며, 이는 요약 정확도에 영향을 미칠 수 있습니다.
+	**비일관성** : 다양한 유형의 문서에서 요약 결과가 일관되지 않을 수 있으며, 특정 주제나 스타일에 따라 다르게 성능을 발휘할 수 있습니다.
+	**극단적 단순화** : 정보의 너무 지나친 단순화로 인해 중요한 세부 사항이 빠지는 경우가 발생할 수 있어, 사용자는 결과를 주의 깊게 검토해야 합니다.
+	**언어적 오류** : 특정 문서에서 문법적 또는 언어적 오류가 발생할 수 있어, 최종 결과물이 고품질일지 보장할 수 없습니다.

---
<a name = "feedback"></a>
# 7. 피드백
사람이 수동으로 요약한 문서와 Llama 3.1이 요약한 문서를 비교할 수 있었다면 더 나은 결과를 얻을 수 있었을 것 같다.
