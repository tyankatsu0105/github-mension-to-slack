# Message to Slack from GitHub

## Concept

```yml
name: Message to Slack from GitHub

on: push

jobs:
  message:
    runs-on: ubuntu-latest

    steps:

      - name: Message
        uses: tyankatsu0105/message-to-slack-from-github@v1
        with: 
          SLACK_WEBHOOK_URL: ${{ secrets.SLACK_WEBHOOK_URL }}
          convert: '[{"tyankatsu0105": "tyankatsu", "ponday_dev": "ponday"}]'
          # ["githubName": "slackName"]
```