# Kaist-Dicia_AI

- Start -
처음 시작할 때 USB 카메라가 아닌 CSI를 사용하기로 했다.
CSI 판을 받아서 Jetson Nano 2GB Developer Kit와 CSI를 조립했다.
엔비디아에서는 Getting Started with Jetson Nano 2GB Developer Kit에서 Micro SD카드 이미지를 다운받았다.
다운 받은 이미지를 압축해제한 뒤에, 준비한 Micro SD카드를 SD CARD formatter를 이용하여 포맷시킨 후
balenaEtcher을 사용하여 포맷한 Micro SD카드에 미리 다운 받아둔 이미지를 굽고 Micro SD 카드를 Jetson Nano 2GB Developer Kit보드에 넣었다.

- Repetition -
컴퓨터와 HDMI선으로 연결하고 실행시켰는데 ERROR 메세지가 떴다.
다시 한번 이미지를 구워 보았는데 계속해서 에러 메세지가 떴고, Chat GPT에 물어보기까지 했다. ![chatgpt1](https://github.com/junichkhun/Kaist-Dicia_AI/assets/93816438/3d6e61f8-a3d6-4c09-b413-d064454e32e0) ![chatgpt2](https://github.com/junichkhun/Kaist-Dicia_AI/assets/93816438/39fc045e-3f5f-481e-996f-2bca0eb9f956)
위 질문에 대한 대답으로 제시된 해답에 따라 하나하나 수정해보며 구웠지만 ERROR 메세지는 계속해서 떴다.
선생님께서 새로 사오신 Micro SD 카드로 실행해 보아도 마찬가지였다.
결국에는 선생님께서 파일 버전을 바꿔 실행해야 한다는 사실을 발견하고 난 뒤에야, 이미지 파일의 버전을 4.6.1에서 4.6으로 바꾼 뒤에 구웠더니 정상적으로 작동했다. 
엎친 데 덮친 격으로, 우리 컴퓨터에서는 HDMI 연결이 제대로 되지 않아 다른 컴퓨터로 실행했다.
아마도 
