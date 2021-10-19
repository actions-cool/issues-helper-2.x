---
toc: menu
---

## Is there a charge for this feature?

GitHub Actions is provided free of charge by GitHub. Among them, the `Private` project has a monthly limit of 2000 times, [see details](https://github.com/settings/billing). The `Public` project is unlimited.

### Is there a rate limit?

Yes. The bottom layer of Action uses GitHub REST API. The general situation is 5000 times per hour. It is basically sufficient in principle, and it is also required to avoid invalid requests when defining Action. [Detailed view](https://docs.github.com/en/rest/overview/resources-in-the-rest-api#rate-limiting).

## Are there any ready-made templates for reference?

Yes.

1. You can use this [GitHub Actions workflow template](https://github.com/actions-cool/.github) repository template
2. Personal exercises and tests [Actions](https://github.com/actions-cool/test-issues-helper) repository
3. You can also refer to the warehouse of [online users](/en-US#-who-is-using)

## I want to pause Actions, is there an easy way?

Yes, you can directly modify `actions`. For example: `actions:'create-comment'` is changed to `actions:'#create-comment'`. It is also convenient for recovery.

## So many versions, how to choose?

You can view the detailed [changelog](/en-US/changelog). The latest releases version is recommended.

## What should I pay attention to when upgrading from v1.x to v2?

There is only one difference between v1.12 and v2.0.0. That is, `require-permission` in `mark-duplicate` has added the default value `write`.

## What should I do if there is no function I want here?

You can submit it in [What do you want?](https://github.com/actions-cool/issues-helper/discussions/18).
