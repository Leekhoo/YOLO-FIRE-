## 2020년 중반 유튜브를 보고 YOLO의 화재 인식 모델을 만들어본 코드입니다.
[따라한 유튜브 링크](https://youtu.be/h56M5iUVgGs?si=3OVYGKPRXZBU3vNX)

### 알고리즘을 로드합니다. 알고리즘을 실행하기 위해서 세개의 파일이 필요합니다.
1. Weight file : 훈련된 model
2. Cfg file : 구성파일. 알고리즘에 관한 모든 설정이 있다.
3. Name files : 알고리즘이 감지할 수 있는 객체의 이름을 포함한다.

네트워크에서 이미지를 바로 사용할 수 없기때문에 먼저 이미지를 Blob으로 변환해야 한다.

Blob은 이미지에서 특징을 잡아내고 크기를 조정하는데 사용된다.

YOLO가 허용하는 세가지 크기
320 × 320 : 작고 정확도는 떨어지지 만 속도 빠름
609 × 609 : 정확도는 더 높지만 속도 느림
416 × 416 : 중간

추가적으로 임계값은 0에서 1사이의 값을 가지는데
1에 가까울수록 탐지 정확도가 높고 , 0에 가까울수록 정확도는 낮아지지만 탐지되는 물체의 수는 많아진다.

최종 출력결과는 아래와 같습니다.

<img width="532" alt="스크린샷 2024-01-28 12 21 21" src="https://github.com/Leekhoo/YOLO-FIRE-/assets/137920352/4fe11467-4767-4327-98bf-5fe14ad10fb8">
