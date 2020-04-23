Protocol
# 뷰

뷰는 앱의 유저 인터패이스(UI)의 일부이고  뷰를 설정하기위해 Modifiers를 제공한다.

# 선언하기

>protocol View

#개요

사용자가 뷰 프로토콜로에서 확인된 형태를 선언함으로서 직접 사용자정의 뷰를 생성할 수 있다.
사용자정의 뷰에 컨텐츠를 제공하기 위해 원하는 본문에 계산된 요소를 적용시키면 된다.

> struct MyView: View {
>     var body: some View {
>         Text("Hello, World!")
>    }
> }

최상위 뷰를 만들기위해서는 한개 또는 여러개의 SwiftUI에서 제공하는 기본 뷰단위를 위에 예제 처럼 글넣기 함수를 를 사용 하거나, 사용자가 만든 사용자정의 뷰를 게층별로 조합하면 된다.

The View protocol provides a large set of modifiers,
뷰 프로토콜은 많은 기본적으로 제공되는 함수들의 프로토콜로 정의된 수정자(modifier)를 제공하는데 이것을 이용하여 위치를 정하고 앱에 레이아웃에 뷰에 설치해서 사용하면된다.  수정(modifier)는 어느 특정 기능을 가지는 다른 뷰안에서 불리워 사용되어 지도록 감사여진 뷰의 인스턴스로 작동하게 된다. 예를 들면, opacity(_:_) 수정자를 일정의 투명도 양과 함께 새로운 뷰가 리턴하도록 택스트 뷰에 추가 할수 있다.