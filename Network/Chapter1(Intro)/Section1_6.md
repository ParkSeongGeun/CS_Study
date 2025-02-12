## 1.6 공격받는 네트워크

- **네트워크 보안 분야** 는 나쁜 친구들이 어떻게 컴퓨터 네트워크를 공격할 수 있는가와, 그러한 공격으로부터 네트워크를 방어할 수 있는가, 혹은 아예 그러한 공격에 영향을 받지 않는 새로운 구조의 설계 등을 다루는 분야다.

**[나쁜 친구들은 인터넷을 통해 여러분의 호스트에 멀웨어(악성코드)를 침투시킬 수 있다.]**

- 인터넷 연결된 장치들은 유해한 데이터인 `멀웨어(malware)`에 노출될 수 있다.
- 멀웨어의 주요 위험:
    - 개인정보 탈취: `스파이웨어`를 통한 파일, 주민번호, 비밀번호, 키스트로크 정보 유출
    - 네트워크 공격: `봇넷(botnet)`을 구성하여 스팸메일 발송 및 `분산 DoS 공격` 수행
    - 전파력: `자기복제(self-replicating)` 기능으로 다른 호스트들을 연쇄적으로 감염

**[나쁜 친구들은 서버와 네트워크 infrastructure를 공격할 수 있다.]**

- DoS(Denial-of-Service) 공격은 크게 3가지 유형으로 분류된다.
    1. **취약성 공격**
        - 특정 순서의 패킷이나 교묘한 메시지를 보내 시스템 중단 유도
        - 애플리케이션/OS 취약점 이용
    2. **대역폭 플러딩**
 
        ![image](https://github.com/user-attachments/assets/7608aa5e-f81f-4778-af53-774f4bc0f9be)

        - 목표 시스템의 대역폭(R bps) 포화를 위해 대량의 패킷 전송
        - DDoS: 다수의 봇넷을 통해 분산 공격 수행
            - 단일 소스 공격은 쉽게 차단 가능
            - 수천 개 호스트로 구성된 봇넷 활용이 일반적
    3. **연결 플러딩**
        - 대량의 TCP 반열림/전열림 연결 생성
- 정상적인 연결 처리 불가능하게 만든다.
- 각 공격 유형별로 다른 방어 전략이 필요하며, 웹/메일/DNS 서버와 기관 네트워크가 주요 공격 대상이 된다.

**[나쁜 친구들은 패킷을 탐지할 수 있다.]**

- **유비쿼터스 인터넷 접속의 보안 취약점과 패킷 스니핑**
    - 패킷 스니퍼는 무선/유선 네트워크에서 전송되는 모든 패킷을 복사해 민감정보 탈취 가능
    - 수동적 도청으로 탐지가 어려움
    - 대응책: 데이터 암호화

**[나쁜 친구들은 여러분이 신뢰하는 사람인 것처럼 위장할 수 있다.]**

- IP spoofing?
    - 가짜 출발지 주소를 가진 패킷을 인터넷으로 전송하는 기술
    - 다른 사용자로 위장하는 대표적인 공격 방법
    - 해결책: 종단 인증(end-point authentication)을 통한 메시지 출처 확인 필요

---

### 인터넷은 처음에 어떻게 보안 문제에 직면하게 되었을까?

- 초기 인터넷은 '상호 신뢰할 수 있는 사용자 그룹'을 전제로 설계되었다.
- 오늘날 인터넷은 ‘상호 신뢰하는 사용자’를 분명히 포함하지 않는다.
    - 오늘날 인터넷 환경은 초기 설계 의도와 달리 다양한 통신 요구가 존재한다.
        - 상호 불신 관계에서의 통신
        - 익명 통신
        - 제3자 중개 통신
- **상호 신뢰하는 사용자 간의 통신은 일반적인 것이 아니라 예외적인 것임을 명심해야 한다.**
