# @appbooster/appbooster-swiftlint-config

Shared SwiftLint config of Appbooster organization

## Installation

1) Install config through CocoaPods:

```
pod 'AppboosterSwiftLintConfig'
```

2) Add to `Target > Build Phases` a new `Run Script Phase` with following block of code:

```
swiftlint="${PODS_ROOT}/SwiftLint/swiftlint"
if which $swiftlint >/dev/null; then
$swiftlint lint --config "${PODS_ROOT}/AppboosterSwiftLintConfig/.swiftlint.yml"
else
echo "warning: SwiftLint not installed, download from https://github.com/realm/SwiftLint"
fi
```
