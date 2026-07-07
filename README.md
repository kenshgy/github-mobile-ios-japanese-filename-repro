# GitHub Mobile iOS Japanese Filename Reproduction

This repository is a minimal public reproduction case for a GitHub Mobile for iOS issue where files with Japanese names are not displayed.

## Environment

- GitHub Mobile for iOS
- App Version: 1.265.0
- Device: iPhone
- iOS Version: 26.5

## Reproduction Structure

```text
.
├── ascii/
│   └── hello.txt
└── 日本語ディレクトリ/
    └── こんにちは.txt
```

## Steps to Reproduce

1. Open this repository in GitHub Mobile for iOS.
2. Navigate to the `日本語ディレクトリ` directory.
3. Compare it with the `ascii` directory.

## Expected Behavior

The file `こんにちは.txt` should be displayed inside the `日本語ディレクトリ` directory.

## Actual Behavior

The `日本語ディレクトリ` directory itself is visible and can be opened, but files with Japanese names are not displayed in GitHub Mobile for iOS.

## Additional Notes

- The same repository displays correctly in Safari using the GitHub web interface.
- Files with ASCII-only names, such as `ascii/hello.txt`, work as expected.
