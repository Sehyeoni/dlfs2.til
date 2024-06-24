# Chapter1 신경망 복습

## 1.1 수학과 파이썬 복습
- vector : 크기와 방향을 가진 양(행벡터, 열벡터)
- matrix : 숫자가 2차원 형태로 늘어선 것
- tensor : 벡터와 행렬을 확장하여 숫자 집합을 N차원으로 표현한 것

## 1.2 신경망의 추론
- 입력층 input layer
- 출력층 output layer
- 은닉층 hidden layer
- weight
- activation function - 가중치*뉴런값의 합에 활성화함수를 적용하여 다음 입력으로 활용
- bias
- fully connected layer
- Affine
- minibatch

- 완전연결계층에 의한 변환은 선형 변환이다. 시그모이드 함수로 비선형 효과를 부여한다.

- forward propagation : 입력층에서 출력층으로 향하는 전파
- backward propagation : 기울기를 반대방향으로 전파

* 이 책에서의 구현 규칙 : 모든 계층은 forward, backward함수, params, grads 인스턴스 변수를 가진다.(일관된 구현, 확장성을 위해 이렇게 하자~)

## 1.3 신경망의 학습
신경망의 학습 : 최적의 매개변수 값을 찾는 작업

- 손실함수 : loss function
multi-class classification 신경망에서는 손실함수로 흔히 교차 엔트로피 오차 cross entropy error를 이용한다.

- softmax layer
- cross entropy error layer
- 위 두 레이어를 통합하면 역전파 계산이 쉬워진다.

- 신경망의 기울기를 구하는 법 : 연쇄 법칙을 활용한 오차역전파법
- 곱셈, 분기, 반복, 덧셈, 행렬곱 MalMul(Matrix Multiply) 역전파

- 가중치 갱신
1. 미니배치
2. 기울기 계산
3. 매개변수 갱신
4. 1~3 반복

- 경사하강법 : Gradient Descent 매개변수를 기울기와 반대방향으로 갱신하여 손실을 줄임
- 확률적경사하강법 stochastic Gradient Descent(SGD) : 무작위로 선택된 미니배치에 대한 기울기를 이용한다.

## 1.4 신경망 구현

- hyper parameter
- epoch : 학습 단위

- decision boundary 신경망이 분리한 영역

## 1.5 계산 고속화
- 비트 정밀도 : 32비트로도 충분하므로 부동소수점 수를 우선으로 사용하여 메모리 관점에서 속도향상.
- GPU : CUDA 쓰자~

# 1.6 정리
- 복습!
