
# Lab 09

## 실습 내용

### **적외선 컨트롤러(IR Controller)**

#### **Submodule 1** : IR Rx Module - Inverted IR Rx Signal
#### **Submodule 2** : Flexible Numerical Display Decoder
#### **Submodule 3** : Flexible Numerical Display Decoder

#### **Top Module** : 저번 시간에 만든 second counter  및 Submodule 1/2를 이용하여 실습 장비의 LED에 맞는 Display Module 설계

### FPGA 실습 : 리모컨을 눌렀을 때, 버튼에 대응하는 특정 숫자를 Display
: NCO(Numerical Controlled Oscillator) 입력 바꿔서 4초 간격으로 증가하는 코드 테스트

## 퀴즈

 ### 아래 코드 일부를 수정하여 다음을 구하시오
 
 ```verilog wire  [41:0] six_digit_seg; assign       six_digit_seg = { 4{7'b0000000}, seg_left, seg_right } ```
 
  > Q1 - 고정 LED (왼쪽 4개) AAAA 출력 : `AA_AA_00`, `AA_AA_01`, `AA_AA_02`, … 순으로 LED 변경

```verilog wire  [41:0] six_digit_seg; assign       six_digit_seg = { 4{7'b1110111}, seg_left, seg_right } ```

> Q2 - 고정 LED 없이 2개의 LED 단위로 1초 Counter 값 표시 : `00_00_00`, `01_01_01`, `02_02_02`, … 순으로 LED 변경

```verilog wire  [41:0] six_digit_seg; assign       six_digit_seg = {seg_left, seg_right, seg_left, seg_right, seg_left, seg_right } ```
 
## 결과
 
### **Top Module 의 DUT/TestBench Code 및 Waveform 검증**
>DUT/T


### **FPGA 동작 사진 (3개- 일반, Q1, Q2)**
`Please fill up your source`


> Written with [StackEdit](https://stackedit.io/).
<!--stackedit_data:
eyJoaXN0b3J5IjpbMTYwNjU0ODc0NSwtMTQ4NzcyMDE1MywtMj
AwMTUxMTAxOSwtMTg0MjMxMTQ1MV19
-->