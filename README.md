name: Add mask
on: push
jobs:
  log:
    runs-on: ubuntu-latest
    env:
      PASSWORD: SuperSecretValue
    steps:
      - run: echo "::add-mask::${PASSWORD}" # ログ出力時にマスク
      - run: echo "${PASSWORD}"
