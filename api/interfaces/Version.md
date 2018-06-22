[MAheui](../../README.md) / [API](../README.md/) / [interfaces/Version](./Version.md)

# Version

유의적 버전을 준수하는 값 객체입니다.

## Constructor

### Version(major: Int, minor: Int, patch: Int, preRelease: String?, buildMetadata: String?)

### Version(identifier: String)

## Properties

### major
```kotlin
val major: Int
```

주 버전입니다.

### minor
```kotlin
val minor: Int
```

부 버전입니다.

### patch
```kotlin
val patch: Int
```

수 버전입니다.

### preRelease
```kotlin
val preRelease: String?
```

프리 릴리즈 식별자입니다.

### buildMetadata
```kotlin
val buildMetadata: String?
```

빌드 메타데이터입니다.

