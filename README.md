# salesforce-cli-zsh-completion

<img width="600" alt="sfdx-cli-automation" src="https://user-images.githubusercontent.com/746259/34641780-083a2224-f2be-11e7-840a-55833e674ef0.gif">

Both the Zsh command completion for the Salesforce CLI and a script for generating it.

## Dependencies

- Salesforce CLI : [download](https://developer.salesforce.com/tools/sfdxcli)
- jq : [download](https://stedolan.github.io/jq/)

Note: you only need `jq` if you plan to run the script to generate the completion file. If not, you only need the CLI. (But `jq` is pretty awesome, so you probably want it anyway.)

## Usage

Follow the following steps to use these Salesforce CLI completions in the Zsh.

First, clone the repo locally.

```
git clone git@github.com:wadewegner/salesforce-cli-zsh-completion.git
```

Update your `.zshrc` to include the following:

```
# add custom completion scripts
fpath=({YOURPATH}/salesforce-cli-zsh-completion $fpath)

# compsys initialization
autoload -U compinit
compinit
```

Close and open your terminal.

## Update the Zsh completion file

If you want to update the `_sfdx` completion file, run the following script:

```
./generate.sh
```

This will create a new `_sfdx` file. Close and open your terminal.
