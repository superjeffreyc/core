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
- curl or wget
- git
- If using Cygwin, install dos2unix package
- Make sure you are running as administrator

# To install
- git clone https://github.com/superjeffreyc/core
- cd core
- git checkout local_dependencies
- dos2unix scripts/install-sdk.sh
- scripts/install-sdk.sh

## For Windows, also run ONE of the following (requires curl or wget)
- curl -L https://raw.githubusercontent.com/cloud9ide/sdk-deps-win32/master/install.sh | bash
- wget -O - https://raw.githubusercontent.com/cloud9ide/sdk-deps-win32/master/install.sh | bash

# After install
- node server.js -p 8080 -a
- Go to http://127.0.0.1:8080 in your browser

# Options for running the server
    --settings       Settings file to use
    --help           Show command line options.
    -t               Start in test mode
    -k               Kill tmux server in test mode
    -b               Start the bridge server - to receive commands from the cli  [default: false]
    -w               Workspace directory
    --port           Port
    --debug          Turn debugging on
    --listen         IP address of the server
    --readonly       Run in read only mode
    --packed         Whether to use the packed version.
    --auth           Basic Auth username:password
    --collab         Whether to enable collab.
    --no-cache       Don't use the cached version of CSS

# Issues with vim
Consider using c9 as the default editor:
- npm install -g c9 
- You also need to go to Settings->User Settings->Terminal and check Use Cloud9 as the Default Editor
- c9 [filename]

# Troubleshooting install
- Make sure your PATH system environment variable is set properly
- Make sure you have all the requirements installed

# Error messages when running server.js
- If you get a message along the lines of "SyntaxError: Unexpected token ! in JSON at position 0" in plugins/c9.ide.run/runners-docker/SOMEFILE, open that file with a text editor and verify that it is a path pointing to the corresponding file in the runners folder (e.g. ../runners/SOMEFILE). If it is not, replace the contents of the file with this path.
