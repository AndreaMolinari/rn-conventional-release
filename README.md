# Conventional React Native Release

## Automated Versioning for React Native Apps iOS/Android with Conventional Commits

**Overview:**

"Conventional React Native Release" is a tool designed to streamline the automated versioning process for your React Native applications on both iOS and Android platforms. This action leverages `standard-version` and determines version tags based on `conventional-commits`.

## Key Features

- **Automated Versioning:** Say goodbye to manual version management. This action automates the creation and updating of versions for your React Native apps, following the principles of "Conventional Commits."

- **Custom Releases:** You have complete control over the release type. Specify whether a release is an alpha, beta, release candidate (RC), or even a final release.

- **Flexible Options:** Tailor the release process to suit your project's specific needs. You can choose to create a pre-release, mark it as a draft, or designate it as the initial release.

## Usage

**Requirements:**

- una repo che usa node


**Getting Started:**

1. Ensure that you meet the prerequisites mentioned above.
2. Add this action to your GitHub Actions workflow.
3. Configure the necessary environment variables in your repository, including *VARSLIST* if available.
4. The action will automatically manage Gradle file updates before each build and automate Play Store releases as required.
5. Get the *OUTPUTS*

**VARLIST**
1. **Required**
   - token: Your GitHub Token
2. **Optional**
    - first-release: bool
    - release-as: string
    - pre-release-name: string
    - pre-release-github: bool
    - draft: bool

**OUTPUTS**
  - tag_name: The Tag name
  - release_id: Just created release id
  
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