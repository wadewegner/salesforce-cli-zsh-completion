# salesforce-cli-zsh-completion

![sfdx-cli-automation](https://user-images.githubusercontent.com/746259/34641743-89743d94-f2bd-11e7-9acd-93bd371c168c.gif)

Both the ZSH command completion for the Salesforce CLI and a script for generating it.

## Dependencies

- Salesforce CLI
- jq

## Usage

Follow the following steps to use these Salesforce CLI completions in the ZSH.

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

## Update the ZSH completion file

If you want to update the `_sfdx` completion file, run the following script:

```
./generate.sh
```

This will create a new `_sfdx` file. Close and open your terminal.
