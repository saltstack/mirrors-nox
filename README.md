# nox mirror

Mirror of the nox package for pre-commit

For pre-commit: see https://github.com/pre-commit/pre-commit

Fox nox: https://github.com/theacodes/nox


### Using nox with pre-commit

Add this to your `.pre-commit-config.yaml`:

    -   repo: https://github.com/saltstack/mirrors-nox
        rev: ''  # Use the sha / tag you want to point at
        hooks:
        -   id: nox
            alias: lint-tests
            name: Lint Tests
            files: ^tests/.*\.py$
            args:
              - -e
              - lint-tests-pre-commit
              - --
