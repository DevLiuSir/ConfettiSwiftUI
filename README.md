<p align="center">
<img src="Design/ConfettiAnimation-01.png" height="300"></p>

<p align="center"> <b>ConfettiSwiftUI It's a customizable confetti animations. </b></p>

<p align="center">
<img src="https://badgen.net/badge/icon/apple?icon=apple&label">
<img src="https://img.shields.io/badge/language-SwiftUI-orange.svg">
<a href="https://developer.apple.com/swift/"><img src="https://img.shields.io/badge/swift-5.3+-blue.svg?style=flat"></a>
<img src="https://img.shields.io/badge/xcode-14.1+-yellow.svg">
<img src="https://img.shields.io/badge/build-passing-brightgreen">
<img src="https://img.shields.io/github/languages/top/DevLiuSir/ConfettiSwiftUI?color=blueviolet">
<img src="https://img.shields.io/github/license/DevLiuSir/ConfettiSwiftUI.svg">
<img src="https://img.shields.io/badge/platform-ios%20|macOS-lightgrey.svg">
<img src="https://img.shields.io/github/languages/code-size/DevLiuSir/ConfettiSwiftUI?color=ff69b4&label=codeSize">
<img src="https://badgen.net/github/commits/DevLiuSir/ConfettiSwiftUI">
<img src="https://img.shields.io/github/repo-size/DevLiuSir/ConfettiSwiftUI">
<img src="https://img.shields.io/github/last-commit/DevLiuSir/ConfettiSwiftUI">
<img src="https://img.shields.io/github/commit-activity/m/DevLiuSir/ConfettiSwiftUI">
<img src="https://img.shields.io/github/stars/DevLiuSir/ConfettiSwiftUI.svg?style=social&label=Star">
<img src="https://img.shields.io/github/forks/DevLiuSir/ConfettiSwiftUI?style=social">
<img src="https://img.shields.io/github/watchers/DevLiuSir/ConfettiSwiftUI?style=social">
<a href="https://twitter.com/LiuChuan_"><img src="https://img.shields.io/twitter/follow/LiuChuan_.svg?style=social"></a>
</p>


## Requirements

- iOS 14.0+ | macOS 11+
- Swift 5+

## Parameters

| parameter          | type           | description                                           | default                                                                                              |
| ------------------ | -------------- | ----------------------------------------------------- | ---------------------------------------------------------------------------------------------------- |
| counter            | Binding<Int>   | on any change of this variable triggers the animation | 0                                                                                                    |
| num                | Int            | amount of confettis                                   | 20                                                                                                   |
| confettis          | [ConfettiType] | list of shapes and text                               | [.shape(.circle), .shape(.triangle), .shape(.square), .shape(.slimRectangle), .shape(.roundedCross)] |
| colors             | [Color]        | list of colors applied to the default shapes          | [.blue, .red, .green, .yellow, .pink, .purple, .orange]                                              |
| confettiSize       | CGFloat        | size that confettis and emojis are scaled to          | 10.0                                                                                                 |
| rainHeight         | CGFloat        | vertical distance that confettis pass                 | 600.0                                                                                                |
| fadesOut           | Bool           | size that confettis and emojis are scaled to          | true                                                                                                 |
| opacity            | Double         | maximum opacity during the animation                  | 1.0                                                                                                  |
| openingAngle       | Angle          | boundary that defines the opening angle in degrees    | Angle.degrees(60)                                                                                    |
| closingAngle       | Angle          | boundary that defines the closing angle in degrees    | Angle.degrees(120)                                                                                   |
| radius             | CGFloat        | explosion radius                                      | 300.0                                                                                                |
| repetitions        | Int            | number of repetitions for the explosion               | 0                                                                                                    |
| repetitionInterval | Double         | duration between the repetitions                      | 1.0                                                                                                  |


## Usage

First, add `import ConfettiSwiftUI` on every `swift` file you would like to use `ConfettiSwiftUI`. Define a integer as a state varable which is responsible for triggering the animation. Any change to that variable will span a new animation (increment and decrement).

```swift
import ConfettiSwiftUI
import SwiftUI

struct ContentView: View {
    
    @State private var counter: Int = 0
    
    var body: some View {
        Button("click") {
            counter += 1
        }
        .confettiCannon(counter: $counter)
    }
}

```


## Install

### Swift Package Manager

The [Swift Package Manager](https://swift.org/package-manager/) is a tool for managing the distribution of Swift code. It’s integrated with the Swift build system to automate the process of downloading, compiling, and linking dependencies.

To integrate `ConfettiSwiftUI` into your Xcode project using Xcode 12, specify it in `File > Swift Packages > Add Package Dependency...`:

```swift
https://github.com/DevLiuSir/ConfettiSwiftUI.git, :branch="master"
```

 Official Tutorial [“Swift Package Manager” tab in Xcode](https://developer.apple.com/documentation/xcode/adding_package_dependencies_to_your_app).


## Author
| [<img src="https://avatars2.githubusercontent.com/u/11488337?s=460&v=4" width="120px;"/>](https://github.com/DevLiuSir)  |  [DevLiuSir](https://github.com/DevLiuSir)<br/><br/><sub>Software Engineer</sub><br/> [<img align="center" src="https://cdn.jsdelivr.net/npm/simple-icons@3.0.1/icons/twitter.svg" height="20" width="20"/>][1] [<img align="center" src="https://cdn.jsdelivr.net/npm/simple-icons@3.0.1/icons/github.svg" height="20" width="20"/>][2] [<img align="center" src="https://raw.githubusercontent.com/iconic/open-iconic/master/svg/globe.svg" height="20" width="20"/>][3]|
| :------------: | :------------: |

[1]: https://twitter.com/LiuChuan_
[2]: https://github.com/DevLiuSir
[3]: https://devliusir.com/



## License

`ConfettiSwiftUI` is available under the MIT license. See the [LICENSE](https://github.com/DevLiuSir/ConfettiSwiftUI/blob/master/LICENSE) file for more info.

