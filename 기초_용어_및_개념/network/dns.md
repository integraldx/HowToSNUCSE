# Domain Name System
Domain Name System은 흔히 DNS라고 부르는 것으로 [위키백과](https://en.wikipedia.org/wiki/Domain_Name_System)에 따르면 인터넷이나 private network에 연결된 컴퓨터, 서비스, 혹은 다른 자원들을 위한 계층적이고 분산된 naming system입니다. DNS의 대표적인 역할은 사람이 쉽게 기억할 수 있는 도메인 네임을 IP주소로, 혹은 그 역으로 바꿔주는 것에 있습니다.
도메인 네임의 예시로 웹 브라우저에서 사용하는 URL의 `https://en.wikipedia.org/wiki/Domain_Name_System`에서 `en.wikipedia.org`부분, 마티니 서버에 접속할 때 사용하는 `martini.snucse.org`등이 있습니다.

## DNS Resolve
domain name은 `.`에 의해 구분되는 label들을 가집니다. 가장 오른쪽에 있는 label은 최상위 도메인(top-level domain, TLD)이라 합니다. root domain을 제외한 모든 domain들은 특정 domain의 sub-domain입니다. 어떤 도메인에 왼쪽에 붙는 label은 sub-domain을 구분시켜주는 역할을 합니다. 이러한 구성은 최대 127단계 까지 가능합니다.
즉, `martini.snucse.org`에서 `org`는 최상위 도메인이면서 root domain의 sub-domain입니다. `snucse.org`는 `org`의 sub-domain이고 label `snucse`에 의해 구분됩니다. 마찬가지로 `martini.snucse.org`는 `snucse.org`의 sub-domain입니다. 
domain name를 IP로 바꾸는 과정은 root domain에서 부터 sub-domain으로 내려가는 과정입니다. 과정은 다음과 같습니다.
1. 사용자가 `martini.snucse.org`를 입력합니다.
2. root domain의 name server에 가서 `martini.snucse.org`를 요청합니다.
3. root domain의 name server는 `org` domain의 name server를 가르킵니다.
4. 사용자는 `org` domain의 name server에 가서 `martini.snucse.org`를 요청합니다.
5. 마찬가지로 `org` domain의 name server는 `snucse.org` domain의 name server를 가르킵니다.
6. 사용자는 `snucse.org` domain의 name server에 가서 `martini.snucse.org`를 요청합니다.
7. `snucse.org` domain의 name server에는 `martini.snucse.org`에 대한 IP가 저장되어 있으므로 이를 전달해줍니다.

## 참고자료
[DNS 위키백과](https://en.wikipedia.org/wiki/Domain_Name_System)
AWS DNS 관련 자료
- [한글](https://aws.amazon.com/ko/route53/what-is-dns/)
- [영어](https://aws.amazon.com/route53/what-is-dns/)
[URL 위키백과](https://en.wikipedia.org/wiki/URL)