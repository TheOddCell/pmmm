```
_______________________
\  _ \ \ \ \ \ \ \ \ \ \ Package Manager
 \  __\_\_\_\_\_\_\_\_\_\ Manager Manager
  \_\ A BUR helper
  ```

## What is the BUR?
Check the BUR's repo [here](https://github.com/TheOddCell/bur).

In short: it's the Bedrock Linux equivalent of the AUR - a place where users can publish and share fetch scripts or other utilities, even if it was not officially accepted by [paradigm](https://github.com/paradigm).
## How do I install `pmmm`?
There are 2 methods, using `brl fetch` or installing from source.
You must have git installed for both of these methods.
* Use `brl fetch` if a normal user or BUR developer
* Use installing from source if you are making edits to `pmmm`
### Method 1: `brl fetch`
Download the pmmm file from `https://github.com/TheOddCell/pmmm/blob/main/pmmm` and place it in `/bedrock/share/brl-fetch/distros`, then run `brl fetch pmmm` as root.
### Method 2: Installing from source.
Run the following commands as root:
```
mkdir /bedrock/strata/pmmm
git clone https://github.com/TheOddCell/pmmm.git /bedrock/strata/pmmm
# you may also copy the files you have done your stuff to to this directory instead of git cloning to it
brl show pmmm
brl enable pmmm
git submodule update --remote --merge
```
### Removal
To remove pmmm, run the command `brl remove -d pmmm`. ***This will remove all scripts and not cleanly remove any fetch scripts. Please be sure to remove any installed packages before doing this.***
