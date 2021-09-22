Movie recommendation system using Multimodal input deep learning model
=============

0. Model description

![image](https://user-images.githubusercontent.com/13134929/129929771-f396e0c6-22fe-4aa0-bb96-1cbf0dd30ed7.png)

이 프로젝트는 multimodal input 딥러닝 아키텍처를 사용한 영화추천 시스템이며,
pre-trained된 모델을 사용하실 분들은 하기 파일링크들을 참조부탁드립니다.
코딩 내부의 디렉토리는 제가 쓰는 구글 드라이브 기준으로 작성되어있으니, 용도 것 변경 부탁드립니다.
(코랩 기준으로 작성된 requirements로 pip 설치시 시간에 좀 오래 걸릴 수 있습니다.)

1. Datasets
   0. imdb movies.csv dataset
      - https://www.kaggle.com/stefanoleone992/imdb-extensive-dataset
   0-1. Glove word embedding corpus
      - 파일이름 : glove.6B.100d
      - https://nlp.stanford.edu/projects/glove/

   1. Trained model 
      - Filename : multi_input.h5
      - Download link : https://drive.google.com/file/d/1lQO4XZCry1jLg5_A4Wa8GjkyqiGNfrSl/view?usp=sharing
   2. Preprocessed X_train_images, X_test_images files(구글드라이브에 저장된 4000개의 포스터 이미지를 리사이즈해서 저장한 data입니다.)
      - Filename : X_test_images2.npz
      - Download link : https://drive.google.com/file/d/1-ExagduAfNIPVRPiiMR8dbYUCuW-A9dh/view?usp=sharing
      - Filename :X_train_images2.npz
      - Download link : https://drive.google.com/file/d/1-3XzeFZFFBdTZ1zG3u9LZoORDIvS08hR/view?usp=sharing

2. References
   1. https://towardsdatascience.com/deep-multi-input-models-transfer-learning-for-image-and-word-tag-recognition-7ae0462253dc
   2. https://stackabuse.com/python-for-nlp-movie-sentiment-analysis-using-deep-learning-in-keras/
