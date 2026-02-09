---
source: http://wiki.c2.com/?WorseIsBetter
original_source: https://www.dreamsongs.com/RiseOfWorseIsBetter.html
original_author: Richard P. Gabriel
original_date: "1991"
title: WorseIsBetter
contributors: [MartinPool, SteveFreeman, BenTilly, OmCandea, JanPersson, AnthonyLander, PanuKalliokoski, AsimJalis]
accessed: 2026-02-09
category: foundations
keywords: [Worse is Better, the right thing, simplicity, New Jersey, MIT, Unix, C, Lisp, design philosophy, survival]
summary: "단순하고 실용적인 시스템이 이론적으로 '올바른' 시스템보다 실제로 더 잘 확산된다 — Richard Gabriel의 통찰과 wiki.c2.com 커뮤니티의 토론"
---

# Worse is Better

Richard Gabriel은 1991년 에세이 "Lisp: Good News, Bad News, How to Win Big"에서 두 가지 설계 철학을 대비했다. MIT 접근법은 인터페이스의 단순성, 정확성, 일관성, 완전성을 모두 추구한다. New Jersey 방식은 구현의 단순성을 최우선으로 두고 나머지를 희생한다. Gabriel의 핵심 주장은 역설적이다. "더 나쁜" 시스템이 "더 나은" 생존 특성을 가진다. 단순한 시스템은 바이러스처럼 퍼지고, 퍼진 뒤에 점진 개선된다.

---

## Richard Gabriel의 원본 에세이 (1991)

> **The Rise of Worse is Better**
> by Richard P. Gabriel
> Lucid, Inc.
> {"Lisp: Good News, Bad News, How to Win Big"에서 발췌}

나와 Common Lisp, CLOS 설계자 대부분은 MIT/Stanford식 설계를 깊이 경험했다. 이 스타일의 본질은 "the right thing"으로 요약된다. 이 철학에서는 다음 네 가지를 모두 갖추는 것이 중요하다.

- **단순성(simplicity)** — 설계는 구현과 인터페이스 모두에서 단순해야 한다. 구현보다 인터페이스의 단순성이 더 중요하다.
- **정확성(correctness)** — 설계는 관찰 가능한 모든 측면에서 정확해야 한다. 부정확함을 허용하지 않는다.
- **일관성(consistency)** — 설계에 비일관성이 있어서는 안 된다. 비일관성을 피하기 위해 약간의 단순성과 완전성을 희생할 수 있다. 일관성은 정확성만큼 중요하다.
- **완전성(completeness)** — 설계는 실용적으로 중요한 상황을 가능한 한 많이 다뤄야 한다. 합리적으로 예상 가능한 모든 경우를 처리해야 한다. 단순성을 이유로 완전성을 지나치게 줄여서는 안 된다.

대부분 이 특성들이 좋다는 데 동의할 것이다. 나는 이 설계 철학을 MIT 접근법이라 부르겠다. Common Lisp(과 CLOS), 그리고 Scheme이 MIT 접근법을 대표한다.

Worse-is-better 철학은 약간만 다르다.

- **단순성** — 설계는 구현과 인터페이스 모두에서 단순해야 한다. 인터페이스보다 구현의 단순성이 더 중요하다. 단순성은 설계에서 가장 중요한 고려 사항이다.
- **정확성** — 설계는 관찰 가능한 모든 측면에서 정확해야 한다. 다만 정확성보다 단순성이 약간 더 낫다.
- **일관성** — 설계에 지나친 비일관성이 있어서는 안 된다. 단순성을 위해 일관성을 희생할 수 있다. 드문 상황을 다루는 부분은 아예 빼는 쪽이 낫다. 구현 복잡성이나 비일관성을 도입하는 것보다.
- **완전성** — 설계는 실용적으로 중요한 상황을 가능한 한 많이 다뤄야 한다. 합리적으로 예상 가능한 모든 경우를 처리해야 한다. 하지만 다른 모든 품질을 위해 완전성을 희생할 수 있다. 구현의 단순성이 위태로워지면 완전성을 반드시 희생해야 한다. 단순성을 유지한다면, 완전성을 위해 일관성을 희생할 수도 있다. 특히 인터페이스의 일관성은 가장 가치가 낮다.

초기 Unix와 C가 이 설계 방식의 대표 사례다. 나는 이 전략을 New Jersey 방식이라 부르겠다. 나는 의도적으로 worse-is-better 철학을 과장했다. 나쁜 철학이고 나쁜 접근법이라고 설득하기 위해서다.

그러나 나는 이렇게 믿는다. 허수아비 형태로라도 worse-is-better는 the right thing보다 생존 특성이 더 낫다. 소프트웨어에 적용할 때 New Jersey 방식이 MIT 접근법보다 더 낫다.

### PC loser-ing 이야기

MIT/New Jersey 구분이 실재한다는 걸 보여주는 이야기가 있다. 각 진영의 지지자들은 정말로 자기 철학이 낫다고 믿는다.

두 명의 유명한 사람이 만났다. 한 명은 MIT 출신이다. 다른 한 명은 Berkeley 출신으로 Unix를 만들고 있었다. 그들은 운영체제 문제를 논의했다. MIT 출신은 ITS(MIT AI Lab 운영체제)에 정통했고, Unix 소스코드를 읽고 있었다. 그는 Unix가 PC loser-ing 문제를 어떻게 해결하는지 궁금했다.

PC loser-ing 문제는 이런 상황에서 발생한다. 사용자 프로그램이 시스템 루틴을 호출하여 긴 작업을 수행한다. 이 작업에는 IO 버퍼 같은 중요한 상태가 있을 수 있다. 작업 도중 인터럽트가 발생하면, 사용자 프로그램의 상태를 저장해야 한다. 시스템 루틴 호출은 보통 단일 명령어다. 사용자 프로그램의 PC(Program Counter)만으로는 프로세스 상태를 포착할 수 없다. 시스템 루틴은 작업을 되돌리거나 끝까지 밀고 나가야 한다.

The right thing은 작업을 되돌리는 것이다. 사용자 프로그램의 PC를 시스템 루틴을 호출한 명령어로 복원한다. 그러면 인터럽트 이후 사용자 프로그램이 재개될 때 시스템 루틴에 다시 진입한다. "PC loser-ing"이라 불리는 이유는 PC를 "loser" 모드로 강제하기 때문이다. MIT에서 loser는 user의 애칭이다.

MIT 사람은 이 경우를 처리하는 코드를 찾지 못했다. New Jersey 사람에게 어떻게 처리하는지 물었다. New Jersey 사람은 이렇게 답했다. Unix 개발자들은 이 문제를 알고 있다. 하지만 해결책은 시스템 루틴이 항상 완료하되, 때때로 에러 코드를 반환하는 것이다. 에러 코드는 시스템 루틴이 작업을 완료하지 못했음을 알린다. 올바른 사용자 프로그램은 에러 코드를 확인해야 한다. 필요하면 시스템 루틴을 다시 호출한다.

MIT 사람은 이 해결책이 마음에 들지 않았다. The right thing이 아니었기 때문이다.

New Jersey 사람은 Unix의 해결책이 맞다고 했다. Unix의 설계 철학이 단순성이고, the right thing은 너무 복잡하기 때문이다. 게다가 프로그래머가 이 추가 검사와 루프를 쉽게 넣을 수 있다. MIT 사람은 구현은 단순하지만 기능의 인터페이스는 복잡해졌다고 지적했다. New Jersey 사람은 Unix에서 올바른 트레이드오프를 선택했다고 답했다. 구현의 단순성이 인터페이스의 단순성보다 중요하다.

MIT 사람은 중얼거렸다. "Sometimes it takes a tough man to make a tender chicken." New Jersey 사람은 이해하지 못했다. 나도 잘 모르겠다.

### Worse-is-better가 더 나은 이유

이제 worse-is-better가 왜 더 나은지 주장하겠다. C는 Unix를 작성하기 위해 설계된 프로그래밍 언어다. New Jersey 방식으로 설계되었다. 따라서 C는 괜찮은 컴파일러를 만들기 쉬운 언어다. 프로그래머에게는 컴파일러가 해석하기 쉬운 코드를 작성하도록 요구한다. 어떤 이들은 C를 고급 어셈블리어라고 불렀다. 초기 Unix와 C 컴파일러는 구조가 단순하고 이식이 쉬웠다. 실행에 필요한 머신 자원이 적었다. 운영체제와 프로그래밍 언어에서 원하는 것의 50~80%를 제공한다.

어느 시점이든 존재하는 컴퓨터의 절반은 중간값보다 성능이 낮다. 더 작거나 더 느리다. Unix와 C는 그런 컴퓨터에서도 잘 동작한다. Worse-is-better 철학은 구현의 단순성을 최우선으로 둔다. 따라서 Unix와 C는 그런 머신에 이식하기 쉽다. Unix와 C의 50% 기능이 충분하다면? 어디에나 나타나기 시작할 것이다. 실제로 그렇게 되지 않았나?

**Unix와 C는 궁극의 컴퓨터 바이러스다.**

Worse-is-better 철학의 또 다른 이점이 있다. 프로그래머가 좋은 성능과 적절한 자원 사용을 추구하게 된다. 약간의 안전성과 편의성을 기꺼이 희생한다. New Jersey 방식으로 작성한 프로그램은 작은 머신과 큰 머신 모두에서 잘 동작한다. 코드는 바이러스 위에서 작성되므로 이식성이 좋다.

한 가지 기억할 점이 있다. 초기 바이러스는 기본적으로 좋아야 한다. 그렇다면 이식성만 갖추면 바이러스의 확산은 보장된다. 바이러스가 퍼지고 나면, 개선 압력이 생긴다. 기능을 90%까지 끌어올릴 수도 있다. 하지만 사용자는 이미 the right thing 이하를 수용하는 데 익숙하다.

따라서 worse-is-better 소프트웨어는 다음 순서를 밟는다. 첫째, 수용된다. 둘째, 사용자가 낮은 기대치에 길들여진다. 셋째, 거의 the right thing에 가까운 수준까지 개선된다. 구체적으로 말하겠다. 1987년 Lisp 컴파일러는 C 컴파일러만큼 좋았다. 그런데 C 컴파일러를 개선하려는 전문가가 훨씬 많다.

좋은 소식이 있다. 1995년에 우리는 좋은 운영체제와 프로그래밍 언어를 갖게 될 것이다. 나쁜 소식은 그것이 Unix와 C++이라는 점이다.

### 통합의 전통

Worse-is-better의 마지막 이점이 있다. New Jersey 언어와 시스템은 복잡한 monolithic 소프트웨어를 만들 만큼 강력하지 않다. 따라서 대규모 시스템은 컴포넌트를 재사용하도록 설계해야 한다. 그 결과 통합의 전통이 자연스럽게 생겨난다.

### The right thing의 두 시나리오

The right thing은 어떤가? 두 가지 시나리오가 있다. 크고 복잡한 시스템 시나리오와 보석처럼 정교한 시스템 시나리오다.

크고 복잡한 시스템 시나리오는 이렇다.

먼저 the right thing을 설계해야 한다. 그다음 구현을 설계해야 한다. 마지막으로 구현한다. The right thing이므로 원하는 기능의 거의 100%를 갖추고 있다. 하지만 구현의 단순성은 고려 대상이 아니었으므로 구현에 오래 걸린다. 크고 복잡하다. 제대로 사용하려면 복잡한 도구가 필요하다. 마지막 20%가 전체 노력의 80%를 차지한다. 그래서 the right thing은 나오기까지 오래 걸린다. 가장 고급 하드웨어에서만 제대로 동작한다.

보석처럼 정교한 시스템 시나리오는 이렇다.

The right thing을 설계하는 데 끝없는 시간이 걸린다. 하지만 어느 시점에서든 상당히 작다. 빠르게 실행되도록 구현하는 것은 불가능하거나, 대부분의 구현자 역량을 넘어선다.

이 두 시나리오는 각각 Common Lisp과 Scheme에 해당한다.

첫 번째 시나리오는 고전적인 인공지능 소프트웨어에도 해당한다.

The right thing은 흔히 monolithic한 소프트웨어가 된다. 하지만 꼭 그래야 할 이유는 없다. 단지 the right thing이 monolithic하게 설계되는 경우가 많을 뿐이다. 이 특성은 우연의 산물이다.

### 교훈

여기서 배울 교훈은 이것이다. The right thing을 처음부터 추구하는 것은 바람직하지 않은 경우가 많다. 절반의 해결책을 먼저 바이러스처럼 퍼뜨리는 것이 낫다. 사람들이 거기에 빠지고 나면, 시간을 들여 90%까지 개선하면 된다.

잘못된 교훈은 이 비유를 문자 그대로 받아들이는 것이다. C가 AI 소프트웨어에 적합한 수단이라고 결론 내리면 안 된다. 50% 해결책은 기본적으로 올바라야 한다. 이 경우에는 그렇지 않다.

다만 한 가지 결론은 내릴 수 있다. Lisp 커뮤니티는 Lisp 설계에 대한 입장을 진지하게 재고할 필요가 있다. 이에 대해서는 뒤에서 더 이야기하겠다.

---

## wiki.c2.com 토론

### 두 가지 해석

> 흥미로운 논문이다. 두 가지 이면이 있어 보인다. 하나는 [WorseIsBetter](http://wiki.c2.com/?WorseIsBetter)가 좋은 설계 패턴이라는 해석이다. 단순하고 예측 가능한 시스템부터 시작하라는 것이다. 다른 하나는 위안이다. 좋은 시스템을 만들고도 상업적으로 실패한 사람들을 위한.
>
> -- [MartinPool](http://wiki.c2.com/?MartinPool)

---

### 작게 시작하고 지켜보라

> 한 가지 짚을 점이 있다. [RichardGabriel](http://wiki.c2.com/?RichardGabriel)의 책에 나오는 내용이다. 사용자가 무엇을 가장 원하는지 우리는 정말 모른다. 그러니 최소한의 구현을 최대한 빨리 내놓고, 그다음에 무슨 일이 벌어지는지 지켜보라. [YouArentGonnaNeedIt](http://wiki.c2.com/?YouArentGonnaNeedIt)과 통하는 이야기다. 또한 설계가 작을수록 이식하기 쉽다. 이식하기 쉬우면 더 널리 퍼진다. C가 좋은 예다. 일단 널리 퍼지면, 나머지는 따라온다.
>
> -- [SteveFreeman](http://wiki.c2.com/?SteveFreeman)

---

### Java/C++, Windows/OS/2, 그리고 XP

> 이 문장을 보자. "1987년에 Lisp 컴파일러는 C 컴파일러만큼 좋았다. 그런데 C 컴파일러를 개선하려는 전문가가 훨씬 많다." 여기서 Lisp을 Java로, C를 C++로 바꿔보라. 1987을 올해로 바꿔보라. 뜨거운 토론감이 된다.
>
> Microsoft의 Windows가 IBM의 OS/2를 이긴 것도 떠오른다. 일단 빨리 내놓고, 90%는 나중에 맞추는 것이다.
>
> 지금의 XP 철학도 마찬가지다. 빨리 내놓되, 단순하게, 기대한 대로 기본은 갖춘다. 다음 반복에서 더 낫게 만들면 된다.
>
> -- [OmCandea](http://wiki.c2.com/?OmCandea)

---

### SOAP vs CORBA

> 이 논문의 진실을 보여주는 최근 사례가 있다. SOAP과 CORBA의 비교다. SOAP이 성공한 이유는 단순성이다. 누구나 이해할 수 있을 만큼 단순하다. 그게 널리 퍼진 이유다.
>
> -- [JanPersson](http://wiki.c2.com/?JanPersson)

> "더 나쁜(worse)" 것은 단순한 XML-over-HTTP다. 많은 사람이 SOAP보다 이쪽을 택한다.

---

### 가치 체계의 차이

> 이 논문에 대한 나의 오랜 생각이 있다. 서로 다른 가치 체계의 이야기라는 것이다.
>
> 사람은 "나쁜 것"과 "좋은 것"을 절대적 속성으로 본다. 그렇지 않다. 좋고 나쁨은 가치 체계에 달렸다. 한쪽의 품질과 다른 쪽의 품질을 혼동하기 쉽다. 이 실수는 깊은 혼란을 낳는다.
>
> Lisp은 올바르게 작동하려 하기에 Better다. C는 그렇지 않기에 Worse다. C는 널리 퍼지려 하기에 Better다. Lisp은 그렇지 않기에 Worse다. "역설"은 올바르게 작동하려는 것이 동시에 Worse이면서 Better라는 점이다. 당연하다. 두 판단이 서로 다른 가치 체계에서 나오기 때문이다.
>
> 다른 예를 들겠다. Multics 사람들의 불만을 찾아보라. 오늘날의 운영체제가 Multics 수준의 보안에도 못 미친다고 한다. 인터넷이라는 위험한 환경에서. [RichardGabriel](http://wiki.c2.com/?RichardGabriel)과 같은 불만이다. 다만 그들은 인기와 품질의 차이를 명확히 구분한다. 그래서 논문만큼 재미있지는 않다.
>
> 잠깐 빗나가겠다. Perl은 여러 면에서 나쁜 언어다. 그런데 CPAN은 가장 큰 재사용 컴포넌트 저장소가 됐다. 왜일까? Perl은 커스터마이징하기 꽤 어렵다. ([DamianConway](http://wiki.c2.com/?DamianConway)가 바꿔왔지만.) 팀 생산성에는 나쁜 특성이다. 하지만 팀 간 재사용에는 좋다. 내 컴포넌트가 당신 환경에 자연스럽게 녹아든다. 그 반대도 마찬가지다.
>
> -- [BenTilly](http://wiki.c2.com/?BenTilly)

---

### 경제학이 과학을 이긴다

> 과잉 engineering한 도구는 민첩한 도구를 이길 수 없다. 고객은 신뢰성보다 기능의 양과 저렴한 가격을 택한다. 어느 쪽이 옳다는 게 아니다. 시장의 현실이다. (Apple은 예외일 수 있다. 하지만 매력이 생산성보다 클 수 있다.)
>
> 가상의 예를 들어보겠다.
>
> **Product A** (Unix 진영):
> - 기능 1: 버그율 10
> - 기능 2: 버그율 10
> - 기능 3: 버그율 10
> - 기능 4: 버그율 10
> - 총 버그: 40
>
> **Product B** (MIT 진영):
> - 기능 1: 버그율 3
> - 기능 2: 버그율 3
> - 기능 3: 버그율 40 (수동 수행)
> - 기능 4: 버그율 40 (수동 수행)
> - 총 버그: 86
>
> 고객 관점에서 보면, 기능 부재가 버그보다 더 큰 "품질" 문제다. 빠진 기능을 직접 채워야 하기 때문이다.
>
> "engineering이 과학을 이긴다"는 표현이 있다. 나는 "경제학이 과학을 이긴다"가 맞다고 본다. 선택권이 있다면, 엔지니어는 완벽주의자다. 세부사항을 제대로 하고 싶어 한다. 하지만 시장은 기능, 일정, 가격에도 압력을 가한다. 생명 안전 같은 일부 틈새를 제외하면.

---

## 키워드

Worse is Better, the right thing, simplicity, New Jersey approach, MIT approach, Unix, C, Lisp, design philosophy, survival characteristics, [ExtremeProgramming](http://wiki.c2.com/?ExtremeProgramming), [YouArentGonnaNeedIt](http://wiki.c2.com/?YouArentGonnaNeedIt)

## 관련 문서

- [WhatIsSoftwareDesign](what-is-software-design.md) — Reeves의 "소스 코드가 곧 설계다". 코딩이 설계 활동이라는 주장은 worse-is-better의 "일단 만들고 개선하라"와 공명한다.
- [NoSilverBullet](no-silver-bullet.md) — Brooks의 본질적 복잡성 논의. Worse-is-better는 복잡성에 대한 실용적 전략이다.
- [BigBallOfMud](big-ball-of-mud.md) — 구조 없는 시스템이 현실에서 살아남는 이유. Worse-is-better의 실제 결과물.
- [TheBestIsTheEnemyOfTheGood](http://wiki.c2.com/?TheBestIsTheEnemyOfTheGood) — 볼테르의 격언. 완벽이 좋음의 적이다.
- [GoodEnough](http://wiki.c2.com/?GoodEnough) — "충분히 좋은" 설계에 대한 토론
- [CategoryIdealism](http://wiki.c2.com/?CategoryIdealism), [CategoryQuality](http://wiki.c2.com/?CategoryQuality), [CategoryEconomics](http://wiki.c2.com/?CategoryEconomics)
