# Continuous-Deployment Scripts
STILL IN HEAVY DEVELOPMENT AND NOT READY NOW!
Useat your own risk. :smirk:


## What is it?
Script(s) for continuous deployment (blue-green) on Anynines for usage
with i.e. [Codeship](https://www.codeship.io/)

## How does it work?
The script does following:

1. Download the cf CLI in version 1.6.2
2. Auth your cf user
3. Target your cf organisation and space
4. Precompile your assets
6. Push the not started application (green or blue)
7. Stops the old application (TBD)
8. Push additional applications if setup (like workers, clockwork or so)

## How do i use it?

First of all you have to configure it properly through ENV variables
### Configuration
There are several properties you can/must configure to use this script, here is a table of all available ENV variables.

TBD
