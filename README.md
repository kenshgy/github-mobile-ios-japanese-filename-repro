# GitHub Mobile (iOS) does not display Japanese-named files

## Summary

GitHub Mobile for iOS can display a directory whose name includes Japanese characters, but it does not display files whose names include Japanese characters inside that directory.

## Environment

- GitHub Mobile for iOS
- App Version: 1.265.0
- Device: iPhone
- iOS Version: 26.5

## Public Reproduction Repository

https://github.com/kenshgy/github-mobile-ios-japanese-filename-repro

## Reproduction Structure

```text
.
├── ascii/
│   └── hello.txt
└── 日本語ディレクトリ/
    └── こんにちは.txt
```

## Steps to Reproduce

1. Open the public reproduction repository in GitHub Mobile for iOS.
2. Navigate to the `日本語ディレクトリ` directory.
3. Compare it with the `ascii` directory.

## Expected Behavior

The file `こんにちは.txt` should be displayed inside the `日本語ディレクトリ` directory.

## Actual Behavior

The `日本語ディレクトリ` directory itself is visible and can be opened, but files with Japanese names are not displayed in GitHub Mobile for iOS.

## Additional Notes

- The same repository displays correctly in Safari using the GitHub web interface.
- Files with ASCII-only names, such as `ascii/hello.txt`, work as expected.

Thank you for taking a look.
