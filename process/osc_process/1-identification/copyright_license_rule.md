---
title: Source Code 내 저작권 및 License 표기 규칙
---

# Source Code 내 저작권 및 License 표기 규칙

License는 무엇이고 저작권이 누구에게 있는지 쉽고 명확하게 확인하기 위해서 Source Code 내 저작권과 License를 올바르게 표기해야 합니다. 

Source Code 내 올바른 저작권 및 License 표기를 위해서 다음 세가지 규칙을 준수합니다.      
1. [각 파일에 저작권과 License를 표기합니다.](#1-source-파일-내-저작권license-표기)
2. [(OSS Package가 포함된 경우) Open Source Software Package 정보 파일을 추가합니다.](#2-oss-package-정보-파일-추가)
3. [(Source Code를 배포하는 경우) License 원문 파일을 추가합니다.](#3-license-원문-파일-추가)

## 1. Source 파일 내 저작권/License 표기
Software 개발자는 다음과 같이 Case별로 준수해야 하는 규칙에 따라 저작권 및 License를 표기합니다.

| No  | Case | Rule |
| ------------- | ------------- | ------------- |
| 1 | LG 전자에서 자체 개발한 Source 파일 | 각 파일 상단에 저작권과 License를 표기합니다.  | 
| 2 | Open Source 파일 | Open Source의 저작권 및 License 표기를 수정/삭제하지 않습니다. | 
| 3 | Open Source에서 특정 파일 또는 function만 자사 Source Code에 포함시키는 경우 | 해당 파일에 저작권 및 License 표기가 이미 적절하게 되어 있을 경우, 이를 수정/삭제하지 않습니다. <br><br>해당 파일에 저작권 및 License 표기가 누락되었거나, 특정 function만 복사해서 사용하는 경우, 원 Open Source에 명시된 저작권 및 License를 자사 Software에 포함시킨 파일에 표기합니다.  |  

💁 **License 표기 방법**    
SPDX-License-Identifier: [[SPDX License Identifier](https://spdx.org/licenses/)]     

ex 1. Apache-2.0
```
SPDX-License-Identifier: Apache-2.0
```

ex 2. LGE Proprietary License    
```   
Copyright (c) 2020 LG Electronics Inc.    
SPDX-License-Identifier: LicenseRef-LGE-Proprietary            
```

## 2. OSS Package 정보 파일 추가
[⭐ 이 규칙은 OSS Package가 포함된 경우에만 해당됩니다.]
oss-pkg-info.yaml 파일 (Yaml 형식)을 생성하고, 다음과 같이 OSS Package에 대한 정보를 포함하는 내용을 기재하여 최상단 directory 내 추가합니다. ex) oss-pkg-info.yaml

단, 이미 이와 같은 정보를 포함하고 있는 file(ex-requirements.txt, pom.xml)이 존재한다면 해당 file로 대체 가능합니다.

```
libidn:
- version: "1.5"
  source name or path:
  - a.c
  - b.c
  license:
  - "GPL-3.0"
  - "LGPL-2.1"
  download location: "http://ftp.gnu.org/gnu/libidn"
  homepage: "https://www.gnu.org/software/libidn"
  copyright text: "Copyright (c) 2002-2007, Simon Josefsson"
node-backoff:
- version: "2.5.0"
  source name or path: "src/*"
  license: "MIT"
  download location: "https://github.com/MathieuTurcotte/node-backoff"
  homepage: "https://www.npmjs.com/package/backoff"
  copyright text: "Copyright (c) 2012 Mathieu Turcotte"
  exclude: True
rsync:
- version: "2.6.9"
  source name or path: "test/tool"
  license: "GPL-2.0"
  download location: "https://download.samba.org/pub/rsync/src"
  homepage: "http://rsync.samba.org"
- version: "3.1.2"
  source name or path: "test/tool"
  license: "GPL-3.0"
  download location: "https://download.samba.org/pub/rsync/src"
  homepage: "http://rsync.samba.org"
  copyright text:
  - "Copyright (c) 1996 Andrew Tridgell"
  - "Copyright (c) 1996 Paul Mackerras"
  - "Copyright (c) 2003-2015 Wayne Davison"
```

## 3. License 원문 파일 추가
[⭐ 이 규칙은 Source Code를 배포하는 경우에만 해당됩니다.]

1. Project의 최상위 directory에 해당 Repository의 License를 대표하는 파일을 생성합니다.
    - License 원문 파일을 다운받아 파일명을 LICENSE, LICENSE.md,  LICENSE.txt, NOTICE 중 하나로 지정합니다.
2. Project의 최상위 directory에 LICENSES라는 이름의 directory를 생성하고, Project에 포함된 License의 원문 파일을 포함합니다.
    - Project에 여러 License의 software가 포함된 경우, 각 License의 원문 파일을 모두 포함합니다.
