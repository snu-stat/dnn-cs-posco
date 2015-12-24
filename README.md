# 인공 신경망과 딥 러닝 강의 실습 코드
* [Keras library](http://keras.io)를 이용한 딥 뉴럴 네트워크 실습 코드입니다.
* 해당 코드를 이용해 실습을 진행하기 위해서는 [Python 2.7](https://www.python.org/), [Theano](http://deeplearning.net/software/theano/#), [Keras library](http://keras.io)가 필요합니다.

## 코드 구성
* [mnist_shallow.py](https://github.com/snu-stat/dnn-cs-posco/blob/master/mnist_cnn_sigmoid.py)
    + MNIST 데이터의 구분을 위한 얕은 네트워크(shallow network)를 구성해 훈련하고, 결과를 확인
* [mnist_cnn_sigmoid_shallow.py](https://github.com/snu-stat/dnn-cs-posco/blob/master/mnist_cnn_sigmoid.py)
    + CNN(Convolutional Neural Network) 네트워크 구조를 이용해 MNIST 데이터를 훈련하고, 결과를 확인
    + 계산 유닛으로 sigmoid를 사용
* [mnist_cnn_sigmoid.py](https://github.com/snu-stat/dnn-cs-posco/blob/master/mnist_cnn_sigmoid.py)
    + CNN(Convolutional Neural Network) 네트워크 구조를 더 쌓아 구성한 Deep Convolutional Network를 이용해 MNIST 데이터를 훈련하고, 결과를 확인
    + 계산 유닛으로 sigmoid를 사용
      
## GPU 사용
* GPU 사용이 가능한 컴퓨터의 경우, Theano에서 제공하는 GPU 병렬화 기능을 사용하기 위해서는 Theano flag를 GPU 계산을 위해 셋팅해야 함.
    + 예를 들어 mnist_shallow.py 프로그램을 GPU에서 실행시키려 할 경우, Command-line Prompt에 다음과 같이 입력해 코드를 실행 

```
> THEANO_FLAGS=mode=FAST_RUN,device=gpu,floatX=float32
> python mnist_shallow.py
```    
