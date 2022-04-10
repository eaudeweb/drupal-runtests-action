# Run Drupal 8+ tests

## Usage

```yml
on: [pull_request]
name: Test
jobs:
  qa-tests:
    name: "Run Drupal tests"
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v2
        with:
          fetch-depth: 1

      - name: 'Install dependencies'
        uses: eaudeweb/drupal-install-action@main
        with:
          dev: true

      - name: 'Run Drupal tests'
        uses: eaudeweb/drupal-runtests-action@main
```
