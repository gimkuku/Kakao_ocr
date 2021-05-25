# Kakao_ocr


## Google Colab으로 Kakao OCR 이용하기
​
Kakao API를 이용하기 위해선 developers.kakao 에 등록을 한뒤, 내 프로젝트를 등록하여 rest api key를 받아야 한다. 
​
개발자 등록을 하면 내 애플리케이션 탭에서 애플리케이션을 추가한 뒤 api key를 받을 수 있다.
​
 - 개발자 등록하는 링크 :
​
[https://developers.kakao.com/]



 - 원본 이미지
 
![tofu](https://user-images.githubusercontent.com/52443092/119504331-d32b8e80-bda6-11eb-8229-d9a764737493.jpg)

 - 결과 화면
 
![image](https://user-images.githubusercontent.com/52443092/119504398-e3436e00-bda6-11eb-894e-79a9339f8cf3.png)

 - 결과는 다음과 같이 JSON형식의 file로 나온다.

 - box 범위는 다음과 같이 Integer형식으로 나오는데 나는 이것을 사진에서 어떤 범위인지 사진으로 받고 싶었다.



## 이미지와 인식된 이미지 함께 보기

이미지를 잘라서 확인하려하니, text범위가 사선으로 되어있는 경우 자르기가 애매한 경우가 많았다. 

따라서 사진의 왜곡을 바르게 편 후, 최대한 직사각형의 menu 이미지로 만들어 함수에 넣었다. 

\- 원본 이미지를 org\_img에 넣은 후 파이썬의 slicing\[ : \] 기능을 이용하여 잘라준다. 
​
\- 원본 이미지는 cv2.imread (위에 import 한 cv2 라이브러리의 함수) 를 이용하여 불러왔다. 
​
\- 자른 이미지는 imshow를 이용하여 보여준다. 


 - 결과 화면
 
![image](https://user-images.githubusercontent.com/52443092/119504434-edfe0300-bda6-11eb-8626-806799900758.png)
