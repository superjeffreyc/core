Cloud9 3.0 SDK for Plugin Development
======================================

This fork lets you set up a local Cloud9 without relying on remote dependencies. Currently, the remote dependencies are:

- emmet-core
- nak
- tern
- tern_from_ts

These remote dependencies have been added to the "local_dependencies" branch

======================================

# Requirements
- NodeJS (https://nodejs.org/en/)
- If using Cygwin, install dos2unix package
- Make sure you are running as administrator

# To install
- git clone https://github.com/superjeffreyc/core
- cd core
- git checkout local_dependencies
- dos2unix scripts/install-sdk.sh
- scripts/install-sdk.sh

# After install
- node server.js -p 8080 -a
- Go to http://127.0.0.1:8080 in your browser
