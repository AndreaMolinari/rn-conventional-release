# Conventional React Native Release

## Automated Versioning for React Native Apps iOS/Android with Conventional Commits

**Overview:**

I commit convenzionali scrivono il changelog.
crea il tag, fa la release con quel tag usa changelog come body

## Usage

**Requirements:**

- una repo che usa node


**Getting Started:**

1. Ensure that you meet the prerequisites mentioned above.
2. Add this action to your GitHub Actions workflow.
3. Configure the necessary environment variables in your repository, including *VARSLIST* if available.
4. The action will automatically manage Gradle file updates before each build and automate Play Store releases as required.

**VARLIST**
1. **Required**
   - UNA_COSA
2. **Optional**
   - UNALTRA_COSA


### Usage
```yml
jobs:
  build-android-app:
    runs-on: ubuntu-latest

    steps:
      - uses: actions/checkout@v4
      - uses: actions/setup-node@v3
      - uses: AndreaMolinari/rn-conventional-release@v1.0.0
```

## License
This project is licensed under the MIT License - See the [LICENSE](LICENSE) file for more details.