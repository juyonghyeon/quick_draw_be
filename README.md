# Quick Draw 백엔드

# 1. 개요
Quick Draw에서 사용하는 기능 중 '분류'를 할 수 있도록 하는 작업


# 2. 기획 이유 및 배경
Quick_Draw 프론트엔드 작업, 파이썬을 통한 모델 학습이 끝났다.<br>
이 두 기능을 엮어 CNN을 통한 분류작업을 실행하기 위해 필요한 코드를 작성해보자!

# 3. 기능 설명
다양한 단어를 랜덤으로 출력하여 이용자에게 주제 제공 <br>
주제를 그릴 수 있는 캔버스 <br>
캔버스에 그림을 그리고 '제출'버튼을 누르면 학습된 모델에서 그린 그림이 무엇인지 학습 <br>
한번 더를 누르면 다시 그릴 수 있게 캔버스를 초기화 및 다른 단어를 제공

# 4. 코드 리뷰
## PredictService
실질적인 Quick Draw의 기능을 담당하는 코드

## TruncateService
@Scheduled에 맞춰 일정 시간에 업로드된 파일들을 지우는 코드


## PredictController
PredictService를 제어하는 코드

## Result.js
캔버스에 그린 이미지를 제출할 버튼과 제출후에 일어날 동작을 담당
onRefresh -> 캔버스 초기화 및 새로운 단어 제공 역할

# 5. 구현 화면
https://github.com/juyonghyeon/quick_draw_fe
