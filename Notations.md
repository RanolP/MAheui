# Notations

본 명세 문서에 사용되는 표기들의 뜻 해석입니다.

## \[Class Name\]?

Nullable한 Type을 나타냅니다.

example:
> String?
> →
> `null`이거나 `String`일 수 있는 타입

## \[Class Name\]

Nullable하지 않은 Type을 나타냅니다.

example:
> String
> →
> `String`일 수만 있는 타입

## \[name\]: \[Type\]

이름은 name이고, 타입은 Type인 값을 나타냅니다.

example:
> firstName: String
> →
> 이름이 `firstName`이고, `String`인 값

## val \[name\]: \[Type\]

이름은 name이고, 타입은 Type인 불변 프로퍼티를 나타냅니다.

example:
> val lastName: String?
> →
> 이름이 `lastName`이고, `null`이거나 `String`일 수만 있는 타입인 불변 프로퍼티

## var \[name\]: \[Type\]

이름은 name이고, 타입은 Type인 가변 프로퍼티를 나타냅니다.

example:
> var lastName: String?
> →
> 이름이 `lastName`이고, `null`이거나 `String`일 수만 있는 타입인 가변 프로퍼티

## \[Type\]#\[Method or Property Name\]

해당 타입의 메서드 혹은 프로퍼티를 나타냅니다.
단, 메서드를 나타낼 때는 괄호를 붙이고,
같은 이름의 메서드가 둘 이상일 경우 인자의 타입을 명시합니다.

example:
> Class#getName()
> →
> `Class` 타입의 함수 `getName`
>
> Class#name
> →
> `Class` 타입의 프로퍼티 `name`
