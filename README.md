# build number (with base) action

This action takes two values as input and adds them together.

## NOTE

This was forked from [mlilback/build-number](https://github.com/mlilback/build-number) and modified to use node20 and to add the `run-id` input.

It's worth checking back on the original repo to see if the original author has updated it. I haven't changed the code at all asides from this, so I don't want to maintain this myself - I've done this because we're using it in my current project and I wanted to make sure it was up to date.

[See a PR I created here to address in the original repo](https://github.com/mlilback/build-number/pull/5).

## Inputs

## `base`

**Required** The base build number.

## `run-id`

**Required** The `GITHUB_RUN_NUMBER` which should be provided
as `${GITHUB_RUN_NUMBER}`

## Outputs

## `build-number`

The inputs added together

## environment variable `BUILD_NUMBER`

The inputs added together

## Example usage

```yml
uses: citypaul/build-number@1.0.3
with:
  base: 100
  run-id: ${GITHUB_RUN_NUMBER}
```
