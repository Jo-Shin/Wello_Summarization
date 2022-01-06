## Wello_Summarization
**[Wello](https://welfarehello.com/) & 연세대 데이터 사이언스 학회 DSL 산학협력 프로젝트**

- Wello 정책 데이터 텍스트를 키워드로 요약합니다.
- **Contributors**: 조신형, 김하람, 남영욱, 최연수, 편시현, 허유진
- *보안의 이유로 활용 데이터 및 결과 데이터는 업로드 하지 않았습니다.*

---
### 활용 데이터
- 약 8만개의 정책 데이터
- 정책명, 정책목적, 정책대상, 정책내용 등 정책에 대한 전반적인 내용이 있음
- 복지 성격의 정책이 대부분임 *ex) 재난지원금, 독거노인 지원*

---
### Process
**Word2Vec의 Gensim을 통해, 줄글로 된 정책 text에서 중요한 키워드 5개 추출**
 
1. Korman을 통한 명사 추출
   1) 불용어, 고유어 전처리
   2) 형태소 분석기 Korman을 통해 text 형태소 분석
   3) 명사 추출
2. 정책명, 정책목적을 기반으로 Gensim을 통해 단어의 vector 사전 생성
3. 정책대상/내용에서, 정책명/목적과 가장 유사한 cosine 유사도를 가지는 키워드 추출
 
