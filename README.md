# Axis - A WordPress Plugin Framework
*Korean Korean*

액시스(Axis)는 워드프레스 플러그인 (혹은 템플릿) 개발에서 MVC 패턴을 도입하기 위한 작은 프레임워크입니다.

## 액시스의 목적
액시스의 주 목적은 다음과 같습니다.

  1. 워드프레스 플러그인 개발에 MVC 패턴을 도입.
  1. 워드프레스 플러그인 개발에 있어 수없이 반복되는 코드들에 대한 템플릿 제공
  1. 일부 워드프레스 플러그인 기능에 있어 보다 편리한 기능 제공

### MVC 패턴
액시스는 워드프레스 플러그인, 템플릿 개발에 있어 MVC 패턴을 쉽게 도입하도록 도와줍니다.
 
로딩 속도는 매우 중요한 문제이죠. 사실 워드프레스 플러그인은 워드프레스를 느려지게 만드는 원인이 되고는 합니다.
그래서 사용하지 않는 플러그인은 가급적 비활성화하거나 아예 삭제하기를 권하는 편입니다.
따라서 액시스는 아주 작고 가벼운 프레임워크이면서 MVC 패턴으로 플러그인 개발을 진행할 수 있는 최소한의 것들을 제공하고자 합니다.

### 코드 템플릿
플러그인을 만들게 되면 거의 기본적으로 해야 하는 작업들이 있습니다. 일례로, 메뉴를 생성한다든지, AJAX 콜백 함수를 정의한다든지 하는
것들이죠. 자잘하지만 반드시 처리해야 할 지루한 작업에 대해 액시스는 미리 뼈대 코드를 제공합니다.
이는 마치 플러그인 개발에 있어 미리 '할일 목록'을 만들어 두는 것과 유사합니다. 

### 보다 편리한 기능
워드프레스의 기본 함수 호출을 보다 편리하게 할 수 있도록 도움을 줍니다.
그러나 이 점은 알아두셔야 합니다. 액시스는 MVC 패턴을 도입하기 위한 최소한의 것을 제공하는 작은 프레임워크입니다. 
보다 사용하기 편할수록, 보다 더 비대해지기 마련입니다. 워드프레스의 작은 부분인 플러그인 하나가 지나치게 규모가 커진다면 
조금 문제가 되겠지요.

액시스는 그저 너무나 자주 사용될 법한 어떤 것들에 대한 아주 제한적으로 이러한 기능을 구현할 생각입니다.
모든 기능에 대해 멋진 OOP를 제공한다든지, 가령 Microsoft Windows API에 대해 MFC 가 덧대여졌던 것처럼
액시스가 워드프레스에 대해 어떤 멋진 OOP 가이드를 해 주는 역할은 되지 않을 것입니다.

## 도와 주세요!
액시스는 LGPL을 따릅니다. 어디든지 무료로 사용하실 수 있습니다, 그러나 사용하실 때에는 저자인 저, 남창우(cs.chwnam@gmail.com)에게
사용 사실을 알려 주세요.

사용하신 이의 피드백과 기능 제안을 환영합니다.

## 액시스 사용하기

### 설치
액시스는 git를 통해 다운로드 받을 수 있습니다.

``git clone https://github.com/chwnam/axis.git``

액시스는 서버에서 접근할 수 있다면 어디에든 놓고 사용해도 무방합니다. 다만 액시스 기반의 플러그인을 공식적으로 배포하려면,
액시스를 플러그인 디렉토리 내부에 두고 같이 배포해야 합니다. (사용자들이 여러분의 플러그인을 위해 별도로 액시스를 설치하게 만들 수는 없으니까요)

한편 액시스는 워드프레스 플러그인이 아닙니다. 그러므로 여러 플러그인을 액시스 기반으로 개발하더라도
각각의 플러그인이 액시스를 각자 가져야 할 필요가 없습니다. 가령 서버의 어느 단 한 곳에 액시스 프레임워크를
두고 모든 개발 중인 플러그인이 그 경로만을 참조하는 방식을 쓰더라도 문제 없습니다.
WP_CONTENT_DIR 경로에 axis를 설치해 두는 것을 권장합니다. 

### 샘플 코드
액시스의 sample 디렉토리에 간단하게 액시스를 사용한 플러그인 예제가 수록되어 있습니다.