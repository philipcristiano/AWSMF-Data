# AWSMF-Data

AWSMF-Data is a small SMF script that will execute the user-data from the AWS Metadata API.

## Bootstrap

This will likely be installed into an Illumos image with Packer [see this for an example](https://github.com/philipcristiano/packer-omnios). At the moment this isn't packaged but can be installed with

`curl https://raw.githubusercontent.com/philipcristiano/AWSMF-Data/master/install | bash`

## Behavior

This will attempt to execute the user-data via Bash with a timeout of 15 minutes. If the timeout is reached, SMF will attempt again to execute the script.
