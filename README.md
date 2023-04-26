# pre-commit-message-regex
Automatically abort commit if the commit message does not match the regular expression.
Please use this for commit consistency.


## How to use
1. Install `pre-commit`
   ```shell
   brew install pre-commit # you can install pre-commit using python3
   pre-commit install --hook-type commit-msg
   ```
2. Add `.pre-commit-config.yaml` file in your repository
   ```yaml
     - repo: https://github.com/ruby-kim/pre-commit-message-regex
       rev: REV_NUMBER
       hooks:
         - id: commit-message
           stages: [commit-msg]
           args:
             - --commit-regex=YOUR_REGEX
   ```
