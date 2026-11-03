<p>
<picture>
  <source media="(prefers-color-scheme: dark)" srcset="chagok-banner-dark.svg">
  <img src="chagok-banner.svg" alt="차곡. 외관은 사진이, 기능은 차가 기록합니다. 렌터카 인수·반납 기록 Pleos 차량 앱" width="100%">
</picture>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Pleos_Connect-%EC%B0%A8%EB%9F%89_%EC%95%B1-14191C?style=flat-square" alt="Pleos Connect 차량 앱">
  <img src="https://img.shields.io/badge/Kotlin-2.3-14191C?style=flat-square&logo=kotlin&logoColor=white" alt="Kotlin 2.3">
  <img src="https://img.shields.io/badge/Jetpack_Compose-UI-14191C?style=flat-square&logo=jetpackcompose&logoColor=white" alt="Jetpack Compose">
  <img src="https://img.shields.io/badge/%EC%83%81%ED%83%9C-%EC%97%90%EB%AE%AC%EB%A0%88%EC%9D%B4%ED%84%B0_%ED%99%95%EC%9D%B8_%C2%B7_%EC%8B%A4%EC%B0%A8_%EB%AF%B8%EC%8B%9C%ED%97%98-EC9846?style=flat-square" alt="상태: 에뮬레이터 확인, 실차 미시험">
</p>

차곡은 렌터카를 인수하고 반납할 때 차의 기능 상태를 차가 직접 읽어 기록하는 Pleos 차량 앱입니다. 현대자동차그룹 Pleos 앱 공모전 출품작이며, 현대자동차그룹이 만들거나 운영하는 서비스는 아닙니다.

## 왜 만드나요

렌터카는 빌려줄 때와 돌려받을 때 차 상태를 확인해야 합니다. 그런데 연료·배터리 잔량, 경고등, 소모품 같은 기능 상태는 지금도 사람의 눈과 사진으로 기록됩니다. 그래서 고객은 스스로 증거를 남겨야 하고, 업체는 검수 인력을 쓰면서 확인 책임까지 집니다.

**이 값은 차가 이미 알고 있습니다.**

## 어떻게 하나요

<table>
  <tr>
    <td width="88" valign="top"><img src="step-1-pickup.svg" width="72" alt=""></td>
    <td valign="top"><sub>01</sub><br><b>인수</b><br>차가 잔량, 주행거리, 경고등, 타이어, 문·창문·트렁크·라이트 상태를 읽어 기록합니다. 고객은 QR로 같은 기록을 자기 휴대폰에 받습니다.</td>
  </tr>
  <tr>
    <td width="88" valign="top"><img src="step-2-rental.svg" width="72" alt=""></td>
    <td valign="top"><sub>02</sub><br><b>대여 중</b><br>경고등·소모품·에어백 변화를 이어서 기록합니다. 앱이 꺼져 있던 구간은 '변화 없음'이 아니라 기록 공백으로 남깁니다.</td>
  </tr>
  <tr>
    <td width="88" valign="top"><img src="step-3-return-check.svg" width="72" alt=""></td>
    <td valign="top"><sub>03</sub><br><b>반납 체크</b><br>열린 곳과 켜진 라이트를 차 그림 위에 보여 줍니다. 고치면 바로 다시 확인해 말로 알려 주고, 확인할 것이 없으면 '네'라고 답해 기록을 남깁니다.</td>
  </tr>
  <tr>
    <td width="88" valign="top"><img src="step-4-report.svg" width="72" alt=""></td>
    <td valign="top"><sub>04</sub><br><b>리포트</b><br>인수 때와 비교한 표와 참고 정산을 보여 줍니다. 차 화면과 고객 휴대폰에 같은 무결성 값이 찍혀 같은 기록임을 알 수 있습니다.</td>
  </tr>
</table>

외관 손상 판정은 사진의 몫이고, 책임 소재와 수리비 판단은 업체의 몫이라 다루지 않습니다.

## 기록하는 것과 하지 않는 것

| 기록합니다 | 기록하지 않습니다 |
|---|---|
| 잔량·주행거리, 경고등, 소모품, 타이어, 에어백, 문·창문·트렁크·충전구·라이트 | 위치, 이름·연락처, 음성 원문, 운전 습관 |

- 고객 리포트는 QR 링크의 `#` 뒤에 담깁니다. 이 부분은 서버로 보내지지 않아 기록은 휴대폰 안에서만 열립니다.
- 마이크는 '반납 기록을 남길까요?' 뒤 5초만 켭니다.
- 차에 없는 값은 칸을 만들지 않고, 읽다가 실패한 값은 '확인 불가'로 남깁니다.

## 지금 상태

> [!NOTE]
> Pleos Connect 에뮬레이터에서 동작을 확인했고, 실차에서는 아직 시험하지 않았습니다. 시연 값은 Virtual Console로 주입하며, 앱은 화면과 기록에 에뮬레이터 값임을 밝힙니다.

## 저장소

- **[chagok](https://github.com/HyundaiChagok/chagok)**: 차량 앱과 고객 리포트 웹. Kotlin, Jetpack Compose, Pleos SDK(Vehicle·TextToSpeech·SpeechToText·NaviHelper), Gleo
- **[chagok-docs](https://github.com/HyundaiChagok/chagok-docs)**: 문제 정의서, 요구사항 정의서, 기능 정의서, 화면 캡처

두 저장소는 비공개입니다.
