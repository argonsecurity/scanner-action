# Argon scanner action

Protect the first phase of your software supply chain

## Inputs

#### `argon-token`

**Required** Token provided by argon. This is sensitive, add this as a secret

#### `scanners`

Multiline list of checks to run. Defaults to all.

#### `audit-only`

If true the action will never fail the workflow. Defaults to false.

#### `should-notify`

If true a notification will be sent to the configured Slack/Teams channel on new findings. Defaults to false.

## Example usage

```
uses: actions/argon-scanner@v1
with:
  audit-only: true
  should-notify: true
  argon-token: "${{ secrets.ARGON_TOKEN }}"
```
