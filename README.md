# Kaist-Dicia_AI

- 목표: Jetson Nano 2GB Developer Kit로 이미지 인식하기
- Start -
https://www.gloriouscoding.com/f85008b6-4a64-4b41-90a7-17ee121bab47
처음 시작할 때 USB 카메라가 아닌 CSI를 사용하기로 했다.
CSI 판을 받아서 Jetson Nano 2GB Developer Kit와 CSI를 조립했다.
엔비디아에서는 Getting Started with Jetson Nano 2GB Developer Kit에서 Micro SD카드 이미지를 다운받았다.
다운 받은 이미지를 압축해제한 뒤에, 준비한 Micro SD카드를 SD CARD formatter를 이용하여 포맷시킨 후
balenaEtcher을 사용하여 포맷한 Micro SD카드에 미리 다운 받아둔 이미지를 굽고 Micro SD 카드를 Jetson Nano 2GB Developer Kit보드에 넣었다.

- Repetition -
컴퓨터와 HDMI선으로 연결하고 실행시켰는데 ERROR 메세지가 떴다.
다시 한번 이미지를 구워 보았는데 계속해서 에러 메세지가 떴고, Chat GPT에 물어보기까지 했다.

![chatgpt1](https://github.com/junichkhun/Kaist-Dicia_AI/assets/93816438/3d6e61f8-a3d6-4c09-b413-d064454e32e0) 
![chatgpt2](https://github.com/junichkhun/Kaist-Dicia_AI/assets/93816438/39fc045e-3f5f-481e-996f-2bca0eb9f956)

위 질문에 대한 대답으로 제시된 해답에 따라,
 첫번째 오류 원인인 다운로드 오류를 해결해보기 위해서 튜터님께 받았던 이미지 파일이 아닌 엔비디아 사이트에 올라와 있는 이미지 파일을 다운로드 받아서 사용해 보았으나
여전히 오류가 발생했다. 
 이에 두번째 오류 원인인 압축 해제 오류인지 확인해 보기 위해 제대로 작동하는 친구의 이미지 파일과 내가 다시 다운받은 이미지 파일의 MD5 해시값(MD5 메시지 다이제스트 알고리즘은 128비트 해시 값을 생성하는 널리 사용되는 해시 함수입니다.-출처 위키피디아)을 비교하여 보았으나 해시값 비교 결과 해시값의 차이가 없는것으로 보아 압축해제 오류임은 아니라는 것을 알 수 있었다. 
 그래서 이미지 파일이 깨지거나 잘못되지는 않았고, '그럼 SD카드의 포맷이 문젠가?'라는 생각이 들어 SD CARD formatter를 지우고 다시 설치하여 하였음에도 오류가 나서 남아있는 4,5번에서 문제가 나올 것인데, 5번인 호환성 문제는 사실 키트 그대로 사용한 것이기에 가능성이 없다고 판단해서, 설치
 
결국에는 선생님께서 파일 버전을 바꿔 실행해야 한다는 사실을 발견하고 난 뒤에야, 이미지 파일의 버전을 4.6.1에서 4.6으로 바꾼 뒤에 구웠더니 정상적으로 작동했다. 
엎친 데 덮친 격으로, 우리 컴퓨터에서는 HDMI 연결이 제대로 되지 않아 다른 컴퓨터로 실행했다.
아마도 HDMI 연결선 또는 포트의 문제인 것 같다고 판단했다.
다른 컴퓨터로 실행하는 정상적으로 작동했고, 사용자 아이디 등을 설정한 뒤에야 다음 단계로 나아갈 수 있었다.

- Cooling Fan & Camera -
컴퓨터에 Jetson Nano 2GB Developer Kit를 연결한 후, jetson-fan-ctl.glt를 설치하여 Cooling Fan을 작동시켰다.
