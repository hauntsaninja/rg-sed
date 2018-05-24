rg-sed.py

Do you wish ripgrep did sed? Well that's not going to happen (see https://github.com/BurntSushi/ripgrep/issues/74), so instead here is a very thin wrapper for ripgrep that does regex replacement (using ripgrep's --replace flag). If you need something more fully-featured (but much slower), maybe try codemod.py

Example usage:
> rg-sed.py foo bar

> rg-sed.py --ask 'f([aeiou]+)' 'b$1' -t py
