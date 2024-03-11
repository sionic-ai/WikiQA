# WikiQA

## 데이터 구성
 | Class | 개수 |
| --- | --- |
| Location  | 373 (12%) |
| Human | 494 (16%) |
| Numeric | 658 (22%) |
| Abbreviation | 16 (1%) |
| Entity  | 419 (14%) |
| Description  | 1087 (36%) |

# 데이터 특징
- 후보 답변 문장은 키워드 매칭으로 인한 편견을 피하기 위해 Wikipedia 페이지의 요약 문단을 기반으로 문장 생성.

- 크라우드소싱을 통해 각 문장이 질문에 대한 답변인지 여부를 라벨링

- 약 1/3의 질문에는 정답이 포함되어 있지 않아 정답이 존재하는지 감지하는 평가 세트로 활용할 수 있음

# 예제
영어와 한국어 번역문이 병렬로 구성되어 있음
| question_id | question_EN | document_title_EN | answer_EN | label | question | document_title | answer |
| --- | --- | --- | --- | --- | --- | --- | --- |
| Q8 | How are epithelial tissues joined together? | Tissue (biology) | Cross section of sclerenchyma fibers in plant ground tissue | 0 | 상피 조직은 어떻게 결합되나요? | 조직(생물학) | 식물 지상 조직의 경피질 섬유 단면도 |
| Q8 | How are epithelial tissues joined together? | Tissue (biology) | Microscopic view of a histologic specimen of human lung tissue stained with hematoxylin and eosin . | 0 | 상피 조직은 어떻게 결합되나요? | 조직(생물학) | 헤마톡실린과 에오신으로 염색된 인간 폐 조직의 조직학적 표본을 현미경으로 관찰한 모습 . |


# 영어 데이터 링크 
https://huggingface.co/datasets/wiki_qa

# 번역기
반복되는 질문들이 많아서 일관성 있는 번역을 위해 CAT(Computer-assisted translation) 도구 
https://us.cloud.memsource.com/의 기계 번역 엔진	Phrase Language AI 사용

# 관련 논문
```
@inproceedings{yang-etal-2015-wikiqa,
    title = "{W}iki{QA}: A Challenge Dataset for Open-Domain Question Answering",
    author = "Yang, Yi  and
      Yih, Wen-tau  and
      Meek, Christopher",
    editor = "M{\`a}rquez, Llu{\'\i}s  and
      Callison-Burch, Chris  and
      Su, Jian",
    booktitle = "Proceedings of the 2015 Conference on Empirical Methods in Natural Language Processing",
    month = sep,
    year = "2015",
    address = "Lisbon, Portugal",
    publisher = "Association for Computational Linguistics",
    url = "https://aclanthology.org/D15-1237",
    doi = "10.18653/v1/D15-1237",
    pages = "2013--2018",
}
```
