---
sort: 1
---

# 1단계 Identification

1. SW 개발 부서는 Software 개발에 사용할 Open Source와 License를 확인하고 각 Open Source License의 사용 사례별 조건을 고려하여 지식 재산 유출을 방지할 수 있도록 Software를 설계합니다.
   <br>

2. SW 개발 부서는 배포하는 Software에 Open Source가 포함될 경우 적절한 OSS 고지 방법을 검토하여 확정합니다.
   <br>

3. SW 개발 부서는 Source Code 내 저작권 및 License 표기 규칙을 준수합니다.
   <br>

4. SW 개발 부서와 OSC 담당팀은 Open Source 분석을 통해 사용한 Open Source와 License를 식별합니다.
   Open Source 분석 절차 및 방법은 다음과 같습니다.

```note
- **Source Code 분석**
    - Source Code 확인을 통해 사용한 Open Source와 License를 식별하는 절차입니다.
    - 효율적인 Source Code 분석을 위해 [`FOSSLight Source`](https://github.com/fosslight/fosslight_source)툴을 이용하실 수 있습니다.
- **Binary 분석**
    - Software에 포함되는 모든 Binary 파일들의 출처를 확인함으로써 Source Code 분석 절차에서 빠질 수 있는 Open Source까지도 식별하는 절차입니다.
- **Dependency 분석**
    - Dependency 관리를 지원하는 Software 개발 환경에서 Dependency 목록에 대해 Open Source 및 License를 식별하는 절차입니다.
    - 효율적인 Dependency 분석을 위해 [`FOSSLight Dependency`](https://github.com/fosslight/fosslight_dependency)툴을 이용하실 수 있습니다.
```

<br>
<br>

```tip
효율적인 Open Source 분석을 위하여 [Open Source로 공개되어 있는 Tool](../../tool/osc_tool.md)들을 이용하실 수 있습니다.
더 많은 Open Source 툴들에 대한 정보는 [Tool](../../tool/osc_tool.md) 페이지를 참조하시기 바랍니다.
```
