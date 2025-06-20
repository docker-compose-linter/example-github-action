# GitHub Action Example for [DCLint](https://github.com/zavoloklom/docker-compose-linter)

Automate linting as part of your CI/CD pipeline by adding the GitHub Action to your pipeline. This ensures
that your Docker Compose files are always checked for errors before deployment.

```yaml
name: Lint Docker Compose

on:
  push:
    branches:
      - main
  pull_request:

jobs:
  dclint:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
      - uses: docker-compose-linter/dclint-github-action@v{$ACTION_VERSION}
        with:
          path: ./path-to-compose-files/
          recursive: true
```

More usage examples is
in [docker-compose-linter/dclint-github-action](https://github.com/docker-compose-linter/dclint-github-action).

## Pull Request Examples

- [Basic Action with Annotations and Summary](https://github.com/docker-compose-linter/example-github-action/actions/runs/15779875919)
- [Docker Action with Annotations](https://github.com/docker-compose-linter/example-github-action/actions/runs/15780219598)
- [Reviewdog integration with PR Review](https://github.com/docker-compose-linter/example-github-action/pull/3) 

## License

This project is licensed under the MIT License. See the [LICENSE](./LICENSE) file for more information.

## Contacts and Support

If you find this repository helpful, kindly consider showing your appreciation by giving it a star ⭐.

If you have any questions or suggestions, feel free to reach out:

- **Email**: [s.kupletsky@gmail.com](mailto:s.kupletsky@gmail.com)
- **Х/Twitter**: [zavoloklom](https://x.com/zavoloklom)
- **Instagram**: [zavoloklom](https://www.instagram.com/zavoloklom/)
- **GitHub**: [zavoloklom](https://github.com/zavoloklom)

Also, you can support this project with a one-time donation or becoming a sponsor:

[![PayPal](https://img.shields.io/badge/PayPal-00457C?style=for-the-badge&logo=paypal&logoColor=white)](https://www.paypal.com/donate/?hosted_button_id=J8KS3RUFKSHDL)
[![Patreon](https://img.shields.io/badge/Patreon-F96854?style=for-the-badge&logo=patreon&logoColor=white)](https://www.patreon.com/c/zavoloklom)
[![GitHub Sponsors](https://img.shields.io/badge/GitHub%20Sponsors-171515?style=for-the-badge&logo=github&logoColor=white)](https://github.com/sponsors/docker-compose-linter)
[![Open Collective](https://img.shields.io/badge/Open%20Collective-3385FF?style=for-the-badge&logo=opencollective&logoColor=white)](https://opencollective.com/dclint)
