## ADC(Analog Digital Converter)
ADC란 단어 뜻 그대로 아날로그를 디지털로 변환하는 과정을 말한다.
<br>
임베디드 시스템 내에서 처리되는 모든 데이터와 연산 드은 디지털화 되어 처리된다.
<br>
<br>
여기서 아날로그 신호란 연속적인 신호를 말하고, 디지털 신호는 0과 1로 이루어진 시간을 말한다.

<br>

## ADC 단계
아날로그 신호를 디지털화 하기 위해 필터링(Filtering), 표본화(Sampling), 양자화(Quantization), 부호화(Encoding) 총 4단계를 거친다.

<br>

### 1. 필터링(Filtering)
- 본래 신호를 정확히 표본화 하기 위해 잡음 등의 신호를 차단하는 과정
- 아날로그 신호에는 상당한 노이즈가 있어 이러한 노이즈들을 제거하는 과정

<br>

### 2. 표본화(Sampling)
- 비연속적인 아날로그 신호를 주기 마다 전압 값으로 나누어 직선 값으로 표현한 것
- 즉, 비연속적 신호를 x축 간격을 나누어 표현한 것을 말함
> 샘플링 주기 구하는 방법 : 시간 / 횟수 <br>Ex) 1초당 10000번 표본 추출 = T = 1 / 10,000 = 0.1ms

<p align="center">
  <img src="https://github.com/JeHeeYu/FreeRTOS/assets/87363461/28184628-98e3-440e-a227-1d4b6efcb5c5" width="600" height="200">
</p>

<br>

### 3. 양자화(Quantization)
- 표본화에서 얻어진 수치를 대표 값으로 n개의 레벨로 분해, 샘플 값을 근사화 시키는 과정
- 양자화 과정에서 샘플링 신호를 통해 끝수를 버림으로써 근사치를 구함
- ADC의 해상도(Resoultion)이 높을 경우 샘플링 된 신호의 버리는 수들이 작아져 본래 신호를 더 명확히 표현 가능

<p align="center">
  <img src="https://github.com/JeHeeYu/FreeRTOS/assets/87363461/d2c2c84a-b0c0-4548-a015-9e88bd9491aa" width="600" height="200">
</p>

<br>

### 4. 부호화(Encoding)
- 양자화를 통해 근사화된 값을 디지털 신호인 0과 1로 만들어 주는 과정

<p align="center">
  <img src="https://github.com/JeHeeYu/FreeRTOS/assets/87363461/2c9465e8-dc1e-4a25-9210-01e61c7b5108" width="600" height="200">
</p>

<br>

## ADC 해상도(Resolution) 구하기

```
Voltage : 입력 전압
Resolution : ADC 해상도

Example)
Voltage = 3.3V
Resoultion = 12bit

3.3 / 4096 = 0.0008056V = 0.80586mV
```
