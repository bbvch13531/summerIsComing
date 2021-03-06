# summerIsComing
Smart airconditioner controller with raspberry pi in Swift.

Summer weather in Korea is hot like hell fire. That's why I decided to make smart airconditioner controller.

# 부품
- Raspberry pi b+
- 온도 센서 : DS18B20
- IR receiver : KSM-913TE5N
- IR emitter : ~~IR333C/H0/L10~~ Grove infrared emitter

![image1](./Images/requirements.png)

부품 잘못 산것 같다...

# 설계
1. IR receiver로 에어컨 리모콘 신호 받아서 분석하기 (전원, 온도 증가, 온도 감소, 제습기능)
2. IR emitter로 리모콘의 IR 신호를 그대로 보내기
    > GPIO, LIRC 이용하기
3. 서버에서 IR신호 받아서 처리하기.
4. 라즈베리파이에서 인터페이스로 이용할 웹서버 호스팅
5. 웹서버 - 서버 - IR신호 통신
6. (추가) iOS 앱

# Reference
- [IR-Sensor 캡쳐 예제](http://support.thingplus.net/ko/help/code-share.html)  
- [SwiftyGPIO](https://github.com/uraimo/SwiftyGPIO)  
- [RaspberryPi DS18B20 Tutorial](http://www.circuitbasics.com/raspberry-pi-ds18b20-temperature-sensor-tutorial/)  
- [DS18B20](http://www.devicemart.co.kr/goods/view?no=1382718)  
- [DS18B20 Datasheet](https://www.elecrow.com/download/DS18B20.pdf)


## Devlog
06.17. Infrared emitter 잘못 주문해서 다시 삼.
06.19. 점프케이블 잘못 주문함. 암-수 케이블을 사야하는데 수-수 케이블을 사서 연결을 못함.

2020.06.03. 다시 날이 더워져서 레포지터리가 생각남. DS18B20에서 온도 가져오는 gettemp.py 예제 작성
