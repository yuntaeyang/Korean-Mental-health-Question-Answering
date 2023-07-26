## KQMA
## Introduction
* 정신건강에 대한 한국어 질의응답 데이터
* 추출 기반 MRC
* 생성 기반 MRC

## Datasets
데이터 출처 : https://www.hidoc.co.kr/healthqna/list
* Extraction-based MRC는 json 파일을 사용합니다.
* Generation-based MRC는 csv 파일을 사용합니다.
  
├ KQMA_DATA

|   ├KQMA_dataset_final.xlsx (원천 데이터)

├  KQMA_kor_v1_train.json

├  KQMA_kor_v1_dev.json

├  KQMA_kor_v1_train.csv

├  KQMA_kor_v1_dev.csv

### Extraction-based MRC

  cd Extraction-based MRC
  python ./run_QA.py --model_type roberta --model_name_or_path klue/roberta-large --output_dir klue_roberta-KMQA --data_dir data --data_name KMQA --train_file KQMA_kor_v1_train.json --predict_file KQMA_kor_v1_dev.json 

## References
### [Kobert-KorQuAD](https://github.com/monologg/KoBERT-KorQuAD)
### [Kobart-catbot](https://github.com/haven-jeon/KoBART-chatbot)
