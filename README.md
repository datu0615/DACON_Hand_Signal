# DACON_Hand_Signal
![20220524_125903](https://user-images.githubusercontent.com/84311270/169948268-3fad227f-bbdb-4a1d-8de3-d7d777e05c65.png)
교통 수(手) 신호 패턴 영상에서 추출한 이미지 학습 데이터를 활용한 인공지능 모델 기반의 교통 수신호 동작 인식 모델 개발

## Dataset
open  
	|	--	train  
	|			|	--	file_0  
	|			|			|	--		0.png : 연속된 Image 중 첫 번째 이미지 (가장 낮은 숫자)   
	|			|			|	--		1.png : 연속된 Image 중 두 번째 이미지 (두 번째로 낮은 숫자)  
	|			|			|	--		2.png : 연속된 Image 중 세 번째 이미지 (세 번째로 낮은 숫자)  
	|			|			|					...					: 숫자의 크기 순으로 연속된 이미지들이 저장됨  
	|			|			`	--		file_0.json : 폴더명과 동일한 이름의 json 파일  
	|			|													연속된 Iamge에 대한 포괄 정보  
	|			|													action: 연속된 이미지의 교통 수신호 동작  
	|			|													sequence: 이미지에 대한 연속된 정보 (bounding_box, 2d_pos 등)  
	|			|													info : 이미지의 기타 정보들  
	|			`	--	file_141  
	|	--	test  
	|			|	--	file_142  
	|			|			|	--		0.png  
	|			|			|	--		1.png  
	|			|			|	--		2.png  
	|			|			|					...  
	|			|			`	--		file_142.json  
	|			`	--	file_186  
	|  
	|	--	action_information.csv 	:	동작에 대한 정보	  
	`	--	sample_submission.csv	:	제출 파일 Sample_submission  
  
  ## Model
  다양한 Data Augmentation을 사용하여 데이터를 증강시키고 InceptionV3 모델을 사용하여 학습을 진행
  

  
