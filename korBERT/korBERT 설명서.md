# ENTRI에서 제공하는 korBERT 모델을 사용하였습니다.
1. http://aiopen.etri.re.kr/ 에 들어가서 키를 발급받고 korBERT 파일 다운로드(규정상 파일을 올리지 못했습니다.)
2. korBERT에서 제공하는 파일은 
   형태소분석 결과 기반 BERT 학습 모델(pytorch, tensorflow)/어절 기반 BERT 학습 모델 (형태소분석 미수행)(pytorch, tensorflow)
   여기서는 형태소분석 결과 기반 BERT 학습 모델(tensorflow) 사용
    - 파일: tensorflow 모델 파일 / vocab 파일 / bert_config 파일 / 형태소분석 결과 기반 tokenizer 소스 코드 (tensorflow 버전)
   
   형태소분석기 사용 - OpenAPI 사이트의 형태소분석 API 이용 http://aiopen.etri.re.kr/

3. https://github.com/google-research/bert에서 git clone
4. BERT 파일에 bert_config 파일, vocab파일 그대로 이동
5. tokenizer(src_tokenizer폴더 안 tokenization_morp) 파일은 내용을 복사해서 bert의 tokenizer파일(tokenization)에 덮어쓰기 or
   그대로 복사해서 파일마다 import 명 바꾸기
   (깃허브 코드는 후자의 방식 사용)
   
   tensorflow 모델 파일은 checkpoint폴더 생성 후 폴더 안으로 이동
   
6. 나머지는 코드 참조
   
