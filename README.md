# Bitwarden Clipboard Integration Tool

It's a "fork" of the [Interactive Bitwarden CLI Clipboard Selection](https://gist.github.com/loeschzwerg/c2b9d0b50f712a026aa6454af3b58598) gist from [@loeschzwerg](https://github.com/loeschzwerg).

This tool continues the concept of combining `jq`, `fzf`, and `xclip`, while eliminating the need for manual management of the Bitwarden CLI session key by securely storing it in the home directory, with `sudo` required for access.

## Requirements

- You need the Bitwarden CLI availible as `bw`.
- `jq` redirects the output into selectable snippets.
- `fzf` selects the entry.
- `xclip` copies the selected entry into your clipboard.

## Installation

Copy the script to any directory included in your $PATH.

## Output Example

```
$ bwc github                     
[sudo] password for $USER: 
Using the existing session key from "/home/$USER/.bitwarden_session".
Searching for 'github'...

abcdefgh-ijkl-mnop-qrst-uvwxyz123456
github.com

Username "Username" copied to clipboard.
Press any key to copy the password...
Password copied to clipboard.
```
