---
marp: true
---

<!-- _class: lead -->

# .NET 6 Minimal API

## 개요와 기본 구성 요소
## 예제를 통해 Minimal API 작성 방법 설명
## 구현 팁
## Minimal API가 다른 개발자들에게 미치는 영향

---

<!-- _class: lead -->

## 개요

- .NET 6 Minimal API는 ASP.NET Core에서 새롭게 추가된 기능입니다.
- 훨씬 더 간단하고 직관적인 API를 작성할 수 있도록 해줍니다.
- Minimal API는 Microsoft.AspNetCore.Components.WebAssembly.Authentication 패키지와 함께 사용할 때 특히 유용합니다.

---

<!-- _class: lead -->

## 기본 구성 요소

- Program.cs 파일: ASP.NET Core Minimal API의 진입점입니다.
- Endpoints.MapGet() 메서드: HTTP GET 요청을 처리하는 메서드입니다.
- Endpoints.MapPost() 메서드: HTTP POST 요청을 처리하는 메서드입니다.
- HttpReponseTypeAttribute: Minimal API에서 반환되는 HTTP 응답의 형식을 정의합니다.
- MapControllers() 메서드: ASP.NET Core에서는 기본적으로 컨트롤러가 필요하지만, Minimal API에서는 컨트롤러를 작성하지 않고도 API를 만들 수 있습니다.

---

<!-- _class: lead -->

## 예제를 통해 Minimal API 작성 방법 설명

- 설명 자료는 다른 화면을 이용해서 구성

---

<!-- _class: lead -->

## 구현 팁

- 예제를 통한 간략한 설명

--- 


<!-- _class: lead -->


## Minimal API가 다른 개발자들에게 미치는 영향
- Minimal API는 ASP.NET Core에서 새롭게 추가된 기능 중 하나입니다. 이전에는 ASP.NET Core에서 API를 작성할 때 컨트롤러를 작성해야 했습니다. 하지만 Minimal API를 사용하면 컨트롤러를 작성하지 않고도 더욱 간단하고 직관적인 API를 작성할 수 있습니다. 이는 다음과 같은 영향을 미칠 수 있습니다.

---

<!-- _class: lead -->



- 개발자들은 더욱 간편하게 API를 작성할 수 있게 됩니다.
- API 개발 속도가 빨라지고, 코드를 유지보수하기 쉬워집니다.
- Minimal API는 클라우드 기반 마이크로서비스 아키텍처에서 작은 규모의 서비스를 작성하는 데 특히 유용합니다.

---


<!-- _class: lead -->

Minimal API의 미래 전망
- Minimal API는 ASP.NET Core의 발전과 함께 더욱 중요한 역할을 할 것으로 기대됩니다. 현재는 기본적인 HTTP 요청을 처리하는 Endpoints.MapGet() 및 Endpoints.MapPost() 메서드만 지원하지만, 앞으로 더 많은 HTTP 메서드와 기능이 추가될 것으로 예상됩니다. 예를 들어, API 버전 관리 및 API 문서 생성과 같은 추가 기능이 예정되어 있습니다. 이러한 기능이 추가되면 Minimal API는 더욱 더 확장 가능하고 유연한 API 개발 플랫폼으로 자리 잡을 것입니다.

따라서, Minimal API는 개발자들에게 높은 생산성과 효율성을 제공하며, ASP.NET Core의 발전과 함께 더욱 중요한 역할을 할 것으로 기대됩니다.

