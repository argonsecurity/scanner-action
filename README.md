# Argon Scanner action

This action scans code for vulnerabilities.

## Inputs

## `argon-token`

**Required** Token provided by Argon. It is highly recommended to add it as a secret.

## `scanners`

Multiline list of scanners to run. ie: sast, iac, dockerfiles, etc... defaults to all scanners.

## `audit-only`

If true the action will never fail the workflow. defaults to false.

## `should-notify`

If true a notification will be sent to the Slack/Teams channel of the customer when there are new findings. defaults to false.

## Example usage

```
uses: actions/argon-scanner@v1
with:
  scanners: |
    iac
    sast
  audit-only: true
  should-notify: true
  argon-token: "${{ secrets.ARGON_TOKEN }}"
```
