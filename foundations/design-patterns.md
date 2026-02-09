---
source: http://wiki.c2.com/?DesignPatterns
title: DesignPatterns
contributors: [ChristopherAlexander, FlavioPoletti, KyleBrown, AdewaleOshineye, MarnenLaibowKoser, ScottWalters, MikeHowells, MihalyElekes, GastonNusimovich, JoeBradley, TomPassin]
accessed: 2026-02-09
category: foundations
keywords: [Design Patterns, GoF, Gang of Four, Christopher Alexander, Pattern Language, pattern catalog, AntiPattern, creational patterns, language features]
summary: "Christopher Alexander의 패턴 개념과 GoF의 소프트웨어 Design Patterns 사이의 관계, 패턴의 본질과 한계에 대한 커뮤니티 토론"
---

# Design Patterns

Design Patterns은 반복되는 설계 문제의 맥락적 해결책이다. Christopher Alexander가 건축에서 처음 제시한 개념을 GoF(Gang of Four)가 소프트웨어 설계에 도입했다. 패턴의 정의, Alexander와 GoF의 차이, 패턴의 본질과 한계를 다룬다. wiki.c2.com 커뮤니티 토론이다.

---

## 두 가지 정의

Design Patterns에는 두 가지 대표적인 정의가 있다.

> 각 패턴은 우리 환경에서 반복해서 나타나는 문제를 서술한다. 그리고 그 문제의 핵심 해법을 제시한다. 이 해법은 같은 방식을 반복하지 않으면서도 백만 번이고 재사용할 수 있다.
> -- [ChristopherAlexander](http://wiki.c2.com/?ChristopherAlexander)

[DesignPatternsBook](http://wiki.c2.com/?DesignPatternsBook)은 이렇게 정의한다.

> Design Pattern은 객체 지향 시스템에서 반복되는 설계 문제를 다룬다. 일반적인 해법을 체계적으로 이름 짓고, 동기를 설명하고, 풀이를 제시한다. 문제와 해법, 적용 시점, 그리고 결과를 서술한다. 구현 힌트와 예제도 제공한다. 해법은 문제를 푸는 객체와 클래스의 일반적 배치다. 특정 맥락에서는 이 해법을 맞춤 적용하여 구현한다.

## 커뮤니티 토론

패턴은 다양한 분야에 적용할 수 있다. [SoftwareDesignPatterns](http://wiki.c2.com/?SoftwareDesignPatterns)과 [ArchitecturalDesignPatterns](http://wiki.c2.com/?ArchitecturalDesignPatterns)을 구분해서 이야기해야 한다는 제안이 있었다. 분야를 넘나드는 보편적 패턴이 있을지는 의문이지만, "메타" 패턴은 있을 수 있다.

### AntiPattern이 더 찾기 쉬운 이유

이 위키에서 [AntiPattern](http://wiki.c2.com/?AntiPattern)이 [DesignPattern](http://wiki.c2.com/?DesignPattern)이나 [AmeliorationPattern](http://wiki.c2.com/?AmeliorationPattern)보다 찾기 쉬운 이유는 무엇일까?

> 자기가 한 일을 돌아보며 "아, 그러지 말았어야 했는데"라고 말하기는 쉽다. 반면 "잘했다. 성공 요인은 이거였다"라고 말하기는 어렵다. 뭘 하지 말라고 알려주는 게 뭘 하라고 알려주는 것보다 쉬운 이치와 같다.

> 코드에 버그를 넣는 방법이 올바른 코드를 쓰는 방법보다 훨씬 많은 것과 같은 이치다. :)
> -- [FlavioPoletti](http://wiki.c2.com/?FlavioPoletti)

> 문제 정의가 해법 탐색보다 먼저다. 성공적인 패턴을 찾으려면 먼저 실패한 접근을 경험해야 한다. 대비가 필요하기 때문이다. 또한 성공하는 방법보다 실패하는 방법이 더 많다는 직관도 설득력이 있다.

[SoftwareDesignPatternsIndex](http://wiki.c2.com/?SoftwareDesignPatternsIndex) 페이지가 유용할 수 있다. [SoftwareDesignPatterns](http://wiki.c2.com/?SoftwareDesignPatterns) 페이지에서 설명하는 software engineering 고유의 패턴을 상당수 나열한다. 이 인덱스는 자동 생성이 아니라 오래된 부분도 있을 수 있다. 누구든 직접 갱신할 수 있다.

### Alexander의 패턴인가, GoF의 패턴인가

> [MarkJasonDominus](http://wiki.c2.com/?MarkJasonDominus)는 5분짜리 강연을 준비한 적이 있다. [SoftwareDesignPatterns](http://wiki.c2.com/?SoftwareDesignPatterns) 운동이 정말 [ChristopherAlexander](http://wiki.c2.com/?ChristopherAlexander)의 본래 취지에 부합하는지 의문을 제기한다. 슬라이드 웹 버전(http://perl.plover.com/yak/design/)에서 대략적인 논지를 파악할 수 있다. 여기 사람들은 이에 대해 어떻게 생각하는가?

> [PerlPatternsRepository](http://wiki.c2.com/?PerlPatternsRepository)인 TinyWiki(http://wiki.slowass.net/?DesignPatterns)가 있다. [ChristopherAlexander](http://wiki.c2.com/?ChristopherAlexander)의 패턴과 [GangOfFour](http://wiki.c2.com/?GangOfFour) 버전의 차이를 열거한다. 흑백으로 나눌 문제는 아니지만, 차이는 분명히 있다. [PerlPatternsRepository](http://wiki.c2.com/?PerlPatternsRepository)가 하는 일을 변호할 필요가 있었던 것 같다.
> -- [ScottWalters](http://wiki.c2.com/?ScottWalters)

> 이건 소프트웨어 패턴 커뮤니티에서 아주 오래된 논쟁이다. 최초의 [PLoP](http://wiki.c2.com/?PLoP)(Pattern Languages of Programs) 학회부터 매번 이 주제가 등장하고 반복됐다. [EuroPLoP](http://wiki.c2.com/?EuroPLoP)에서도 마찬가지였을 것이다. [PatternLanguagesOfPrograms](http://wiki.c2.com/?PatternLanguagesOfPrograms) 학회 자체가 이를 위해 만들어졌다. 커뮤니티를 패턴 카탈로그에서 [PatternLanguages](http://wiki.c2.com/?PatternLanguages)로 이끌려는 목적이었다. 하지만 일부에게는 여전히 부족했다. 패턴 커뮤니티의 합의는 이렇다. "우린 안다... 그래도 우리 갈 길 간다..."
> -- [KyleBrown](http://wiki.c2.com/?KyleBrown)

### GoF의 23가지 패턴을 넘어서

> Gamma 등이 문서화한 23가지 패턴과 크게 다른 Design Pattern을 아직 본 적이 없다. 알고 있다면 여기 링크를 달아 달라. 여러 패턴의 조합으로 만들어진 패턴은 제외한다. 또한 특정 환경에 종속되지 않는 범용 패턴이어야 한다.

> [GangOfFour](http://wiki.c2.com/?GangOfFour) 책이 그 모든 Design Patterns를 발명한 게 아니다. 저자들은 수년에 걸쳐 가장 근본적인 객체 지향 Design Patterns를 찾아내 문서화하려 했다. 충분히 집요한 사람이라면 어떤 패턴이든 23개 중 하나와 연결짓지 못할 리 없다. 게다가 [DesignPatternsBook](http://wiki.c2.com/?DesignPatternsBook)을 읽은 사람은 새 패턴을 23개와의 관계로 파악하려 한다. 새로운 색을 발견하는 것과 같다. 누군가는 항상 "사실 그건 회녹청색일 뿐이야"라고 말할 수 있다.
> -- [AdewaleOshineye](http://wiki.c2.com/?AdewaleOshineye)

> Gamma 등이 패턴을 발명하지 않았다는 점은 이해한다. 하지만 이미 잘 알려진 패턴의 변형을 보고 싶다. 그쪽이 더 교육적이기 때문이다. 23가지 패턴이 잘 알려져 있으므로 관련 패턴을 파악하기가 더 쉽다.

> 흥미로운 질문이다. Gamma 등의 책을 꺼내 뒤표지를 봤다. 23가지 Design Pattern의 다이어그램이 있다. 패턴을 수년간 접하고 나니, 이 23가지 패턴은 낮은 수준으로 느껴진다. 객체 두세 개가 상호작용하는 수준이다.

> 더 높은 수준의 패턴을 찾아 PLoP과 PLoP 2를 꺼냈다. PLoP에서 가장 좋아하는 패턴은 #2번이다. "Tools and Materials 비유에 기반한 도구 구성 및 통합 Pattern Language"다.

> 이것은 Alexander의 개념과 정확히 맞아떨어진다. [PatternLanguage](http://wiki.c2.com/?PatternLanguage)는 모든 수준의 세분화를 포함해야 하기 때문이다. 범용적인 패턴으로 일반적 문제를 다루고, 점점 세밀한 패턴으로 상세 설계 수준까지 내려간다. 이러한 소프트웨어 Design Patterns가 Alexander 의미의 패턴이라는 뜻이다.
> -- [TomPassin](http://wiki.c2.com/?TomPassin)

> 그러고 나서 더 생각해 봤다. 내가 아는 다른 낮은 수준의 패턴이 있을까? 파싱과 상태 기계가 떠올랐다. Gamma 등의 책에 간단한 문법을 파싱하는 [InterpreterPattern](http://wiki.c2.com/?InterpreterPattern)은 있다. 하지만 다른 파서나 상태 기계 패턴은 없는 것 같다.

> VisualWorks Smalltalk에서 복사를 처리하는 방식이 떠올랐다. 빈 새 객체를 만든 뒤 그 객체에 postCopy 메서드를 호출한다. 매우 편리하다. [PostCopyMethod](http://wiki.c2.com/?PostCopyMethod)는 Gamma에 없는 유용하고 단순한 낮은 수준의 패턴 후보다.

> 원래 질문자가 충분히 찾아보지 않은 것 같다. 이 위키에는 수많은 패턴이 논의되어 있다. 대부분 [CategoryPattern](http://wiki.c2.com/?CategoryPattern)에서 찾을 수 있다. [Kent Beck](http://wiki.c2.com/?KentBeck)의 [SmalltalkBestPracticePatterns](http://wiki.c2.com/?SmalltalkBestPracticePatterns)도 있다. [Martin Fowler](http://wiki.c2.com/?MartinFowler)의 [AnalysisPatterns](http://wiki.c2.com/?AnalysisPatterns), [PatternLanguagesOfProgramDesign](http://wiki.c2.com/?PatternLanguagesOfProgramDesign) 시리즈도 있다. 근본적인 프로그래밍 패턴이라 할 수 있는 [ShieldPattern](http://wiki.c2.com/?ShieldPattern)까지 있다.

### 패턴은 언어의 한계를 우회하는 것인가

GoF 패턴 중 상당수는 객체 지향 설계의 본질이 아니라는 주장이 있다. 특정 언어의 한계를 보완하는 것이라는 비판이다. 특히 생성 패턴(creational patterns)이 대표적이다. C++, Java, C# 등에서 생성자가 일반 메서드처럼 동작하지 않는다. 이 문제를 우회하려고 고안했다는 것이다. (참고: [AreDesignPatternsMissingLanguageFeatures](http://wiki.c2.com/?AreDesignPatternsMissingLanguageFeatures))

> 오래되고 약한 주장이다. 패턴을 이해하지 못하거나 해당 언어를 깊이 생각하지 않은 사람들의 논리다. [DesignPatternsSmalltalkCompanion](http://wiki.c2.com/?DesignPatternsSmalltalkCompanion)의 생성 패턴 섹션을 읽어보라. C++ 생성자 문법이 없는 Smalltalk에서도 생성 패턴이 왜 필요한지 설득력 있게 설명한다.
> -- [KyleBrown](http://wiki.c2.com/?KyleBrown)

> 약하다고? 논리의 어디에 허점이 있는가? 나는 생성 패턴 다수에 비슷한 반응을 보인다. 예를 들어 [AbstractFactoryPattern](http://wiki.c2.com/?AbstractFactoryPattern)은 Java에서는 훌륭하다. 그러나 [RubyLanguage](http://wiki.c2.com/?RubyLanguage)나 [SmalltalkLanguage](http://wiki.c2.com/?SmalltalkLanguage)처럼 클래스가 first-class 객체인 언어에서는 거의 불필요하다. 클래스의 정체를 미리 몰라도 메시지를 보낼 수 있기 때문이다. [VisitorPattern](http://wiki.c2.com/?VisitorPattern)도 마찬가지다. closed class를 우회하기 위한 패턴이므로, open class를 지원하는 언어에서는 쓸모가 없다. 물론 [CommandPattern](http://wiki.c2.com/?CommandPattern)처럼 어떤 언어에서든 유용한 패턴도 있다. 하지만 그런 패턴은 소수라고 본다. ([ArguingWithGhosts](http://wiki.c2.com/?ArguingWithGhosts))
> -- [MarnenLaibowKoser](http://wiki.c2.com/?MarnenLaibowKoser)

#### 패턴과 단위 테스트

패턴에 표준 단위 테스트를 붙이자는 제안이 있었다. 아키텍처가 테스트를 통과하면 패턴 적용으로 판별하는 리트머스 시험이다. 하지만 단위 테스트 작성 자체가 테스트 대상 코드만큼 어렵다는 지적도 나왔다. -- [MikeHowells](http://wiki.c2.com/?MikeHowells)

#### 패턴 입문자를 위한 접근

> 패턴 입문자에게는 하향식 접근이 유용하다. 자연에도 패턴이 가득하다는 사실부터 인식시키면, Design Patterns의 중요성을 쉽게 납득시킬 수 있다.
> -- [MihalyElekes](http://wiki.c2.com/?MihalyElekes)

### 패턴은 발견이지 설계가 아니다

> [SoftwareDesignPattern](http://wiki.c2.com/?SoftwareDesignPattern)은 누군가가 "설계"하는 것이 아니다. 발견하는 것이다.
>
> SoftwareDesignPattern은 본질적으로 클래스 간 협력이다. 하지만 아무 클래스 협력이나 패턴이 되는 것은 아니다. 충분히 일반적이어서 다양한 시스템 설계에 적용할 수 있다고 누군가가 확인해야 한다.
>
> 소수의 뛰어난 사람들이 처음 패턴을 식별했다. 돌이켜 보면, 그것들이 가장 쉬운 것이었다. 시간이 흐를수록 남은 패턴은 점점 발견하기 어려워진다. 새 패턴이 줄어드는 건 패턴이 더 없어서가 아니다. 발견에 더 많은 노력이 필요해서다.
> -- [GastonNusimovich](http://wiki.c2.com/?GastonNusimovich)

#### Alexander의 Nature of Order

Christopher Alexander의 "The [NatureOfOrder](http://wiki.c2.com/?NatureOfOrder)" 3권이 2004년 출간되어 전 4권이 완간되었다. 총 2,150페이지에 달하는 이 시리즈는 [PatternLanguage](http://wiki.c2.com/?PatternLanguage)에서 패턴을 선택하고 새 패턴을 만드는 이론적 기반을 제공한다. -- [JoeBradley](http://wiki.c2.com/?JoeBradley)

#### 소프트웨어 특허

Design Patterns이 [SoftwarePatent](http://wiki.c2.com/?SoftwarePatent)나 [LogicPatent](http://wiki.c2.com/?LogicPatent)의 대상이 될 수 있는지 묻는 질문이 있었으나, 답변은 달리지 않았다.

### GoF의 ACM SIGPLAN 수상

2005년 7월, ACM SIGPLAN은 GoF에게 Programming Languages Achievement Award를 수여했다.

> "ACM's Special Interest Group on Programming Languages (SIGPLAN) recently awarded the 2005 Programming Languages Achievement Award to Erich Gamma, Richard Helm, Ralph Johnson, and John Vlissides (known as the 'Gang of Four') for their creation of 'Design Patterns' (the computer science book and the subfield at the intersection of programming languages and software engineering). The annual award recognizes an individual (or individuals) who has (have) made a significant and lasting contribution to the field of programming languages."

ACM SIGPLAN은 프로그래밍 언어 분야에 중대하고 지속적인 기여를 한 인물에게 이 상을 수여한다. GoF는 Design Patterns라는 책을 만들었다. 프로그래밍 언어와 소프트웨어 공학의 교차점에 새 분야를 개척한 공로다.

수상자:
- [ErichGamma](http://wiki.c2.com/?ErichGamma)
- [RichardHelm](http://wiki.c2.com/?RichardHelm)
- [RalphJohnson](http://wiki.c2.com/?RalphJohnson)
- [JohnVlissides](http://wiki.c2.com/?JohnVlissides)

이 수상은 패턴에 관심을 가진 모든 위키 참여자에게 의미 있는 일이다. [PeopleProjectsAndPatterns](http://wiki.c2.com/?PeopleProjectsAndPatterns)에 헌신해온 [WardCunningham](http://wiki.c2.com/?WardCunningham)과 c2 wiki에도 마찬가지다.

---

> wiki에서 Design Patterns 자체를 다루기는 하는 건가? 패턴이 뭔지에 대한 메타 토론만 하는 건 아닌가?

> wiki는 아무것도 "다루지" 않는다. 사람들이 원하는 대로 기여하고, 그것이 수년에 걸쳐 쌓이는 것이다. 여기에는 많은 자료가 있다.

---

## 키워드

Design Patterns, GoF, Gang of Four, Christopher Alexander, Pattern Language, pattern catalog, AntiPattern, creational patterns, language features, 객체 지향, 소프트웨어 설계

## 관련 문서

- [GangOfFour](http://wiki.c2.com/?GangOfFour)
- [DesignPatternsBook](http://wiki.c2.com/?DesignPatternsBook)
- [PrintableDesignPatternReferenceCards](http://wiki.c2.com/?PrintableDesignPatternReferenceCards)
- [CategoryRefactoring](http://wiki.c2.com/?CategoryRefactoring)
- [HypermediaDesignPatternsRepository](http://wiki.c2.com/?HypermediaDesignPatternsRepository)
- [AmeliorationPattern](http://wiki.c2.com/?AmeliorationPattern)
- [DesignPatternsConsideredHarmful](http://wiki.c2.com/?DesignPatternsConsideredHarmful)
- [AreDesignPatternsMissingLanguageFeatures](http://wiki.c2.com/?AreDesignPatternsMissingLanguageFeatures)
- [WhenIsTheUseOfDesignPatternsNotAppropriate](http://wiki.c2.com/?WhenIsTheUseOfDesignPatternsNotAppropriate)
- [SoftwareDesignPatternsIndex](http://wiki.c2.com/?SoftwareDesignPatternsIndex)
- [CategoryPattern](http://wiki.c2.com/?CategoryPattern)
- [Wikipedia: Design pattern](http://en.wikipedia.org/wiki/Design_pattern_(computer_science))
