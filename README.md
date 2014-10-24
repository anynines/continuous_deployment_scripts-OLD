# Continuous-Deployment Scripts

## What is it?
Script(s) for continuous deployment (blue-green) on Anynines for usage
with i.e. [Codeship](https://www.codeship.io/)

## How does it work?
The script does the following:

1. Download the cf CLI in version 1.6.2
2. Auth your cf user
3. Target your cf organisation and space
4. Precompile your assets (Rails only)
6. Push the not started application (green or blue)
7. Stops the old application (green or blue)
8. Push additional applications if setup (like workers, clockwork or so)

## How do i use it?

First of all you have to configure it properly through ENV variables

### Configuration
There are several properties you can/must configure to use this script, here is a table of all available ENV variables.

| ENV name | Description | required |
|:--------:|:-----------:|:--------:|
| CF_USER | Your anynines user to deploy with | yes |
| CF_PASSWORD | The password for your CF_USER | yes |
| CF_ORG | The anynines organisation where you want to push your app(s) | yes |
| CF_SPACE | The anynines space where you want to push your app(s) | yes |
| ADDITIONAL_APPS | You can specify additional applications to push, **seperated by commas** (i.e. workers, clockwork or so) | no |

### Run the script
Copy the `cf_deploy` script into your applications `/script` directory
and setup your CI to run it after testing via:
```shell
  script/cf_deploy
```

## Do you have problems or good ideas?
We were very happy to any kind of feedback or additions.
Just create an issue or provide a pull request. :heart:
