# GitHub Mobile (iOS) does not display files or subdirectories inside Japanese-named directories

## Summary

GitHub Mobile for iOS can display a directory whose name includes Japanese characters, but it does not display the files or subdirectories inside that Japanese-named directory.

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
├── 日本語ディレクトリ/
│   ├── こんにちは.txt
│   └── サブディレクトリ/
│       └── hello.txt
├── 中文目录/
│   └── hello.txt
├── 한글디렉터리/
│   └── hello.txt
└── Кириллическая-папка/
    └── hello.txt
```

## Steps to Reproduce

1. Open the public reproduction repository in GitHub Mobile for iOS.
2. Navigate to the `日本語ディレクトリ` directory.
3. Compare it with the `ascii` directory.
4. Optionally compare the behavior with the other non-ASCII directories:
   - `中文目录`
   - `한글디렉터리`
   - `Кириллическая-папка`
5. Optionally navigate into `日本語ディレクトリ/サブディレクトリ`.

## Expected Behavior

The file `こんにちは.txt` and the subdirectory `サブディレクトリ` should be displayed inside the `日本語ディレクトリ` directory.

## Actual Behavior

The `日本語ディレクトリ` directory itself is visible and can be opened, but the files and subdirectories inside it are not displayed in GitHub Mobile for iOS.

## Additional Notes

- The same repository displays correctly in Safari using the GitHub web interface.
- Files with ASCII-only names, such as `ascii/hello.txt`, work as expected.
- This repository also includes Chinese, Korean, Cyrillic, and nested Japanese-directory cases so the issue can be compared across non-ASCII path names.

Thank you for taking a look.
