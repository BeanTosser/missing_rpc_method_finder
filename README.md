# Missing Monero RPC Method Finder

## What is it?
The Missing Monero RPC Method Finder is a shell script that identifies which commands are missing from the RPC wallet developer documentation file (wallet_rpc.md) by comparing it with the header file (wallet_rpc_server_commands_defs.h) for the Monero RPC wallet server C++ source file (wallet_rpc_server.cpp). The script outputs a list containing every method that appears in the header file but NOT in the documentation to a new text file for easy identification.

## Caveats
* This is a Bash script. It will only run natively in Unix-based operating systems such as Linux or MacOS. An external tool such as [git bash](https://gitforwindows.org#bash)
* This script has a very limited and specific use case. You probably have no use for it as is. I published it to github to illustrate my shell scripting abilities publicly. However, with some scripting knowlege, you could easily adapt the script for other scenarios in which you need to find items that are only present in one of two files.

## Using the Missing Monero RPC Method Finder script
1. Download the script [here]().
2. Download the RPC wallet <a href="https://raw.githubusercontent.com/monero-project/monero/master/src/wallet/wallet_rpc_server_commands_defs.h" download="wallet_server_commands_defs.h">header file</a> and <a href="https://raw.githubusercontent.com/monero-project/monero-site/master/_i18n/en/resources/developer-guides/wallet-rpc.md" download="wallet_rpc.md">documentation</a>.
3. Open a terminal.
4. Navigate to the directory containing the downloaded files.
5. Make the script executable: 
`sudo chmod 700 find_missing_rpc_methods.sh"`
6. Run the script:
`./find_missing_rpc_methods.sh`
