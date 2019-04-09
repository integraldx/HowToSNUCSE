## CLion
### CLion IDE

CLion은 JAVA언어용 IDE인 IntelliJ IDEA로 널리 알려진 Jetbrains 사에서 개발한 C/C++용 통합 개발 환경(IDE) 입니다. C와 C++ (C11과 C++17은 부분적으로 지원), JavaScript, Objective-C, Swift 등을 기본적으로 지원합니다.
교육용 라이센스를 이용해 재학 기간 동안 무료로 사용할 수 있습니다. [Clion 설치 페이지](https://www.jetbrains.com/clion/) 에서 설치할 때 학생 계정을 입력하면 됩니다.
최초 설치 시 컴파일러를 비롯한 툴체인을 설정해야 하며, gcc, Clang, MSVC 컴파일러를 연결할 수 있습니다. 


---

### 장점
CLion은 상당히 많은 기능을 갖춘 IDE로,  원하는 Code Highlighting Style을 자유롭게 지정할 수 있으며 Integer Overflow, Infinite Loop 등 자주 일어나는 실수도 잘 잡아주는 편입니다. Git관련된 기능도 잘 갖추어져 있습니다.
가장 큰 장점으로, Windows, macOS, Linux에 모두 설치가 가능하며 거의 동일한 환경을 제공받을 수 있습니다. C/C++ 전문 IDE 중 하나인 Visual Studio에 비해 갖는 가장 큰 장점이라고 할 수 있겠죠.
또한, 플러그인을 이용하여 기능을 더 확장해서 쓸 수 있습니다. 대표적으로 Verilog support를 설치하면 Verilog 언어에 대한 Code Highlight가 가능하며, R, Rust 관련 플러그인 등 언어별 플러그인이나 단축키 설정 관련 플러그인 등을 통해 개인에게 더 특화된 개발 환경을 사용할 수 있습니다. 단축키 관련 설정의 경우 vim 단축키 플러그인, Emacs 단축키 플러그인 등으로 다른 에디터를 사용하던 사람도 같은 단축키를 그대로 적용할 수 있습니다.
IDE 개발을 지속해왔고, 지속하고 있는 기업의 제품이기 때문에 TroubleShooting을 비롯한 지원을 받기가 비교적 용이하다는 장점도 있습니다.

---
### 단점
Dev-C++, Code::Blocks에 비해서는 무거운 편입니다. Visual Studio에 비해서는 훨씬 가볍지만, 그만큼 기능의 다양성은 떨어집니다. 
또한, 다른 곳에서 프로젝트 전체를 내려받아 추가로 작업하는 경우에는 CMake를 직접 작업해야 합니다. 
