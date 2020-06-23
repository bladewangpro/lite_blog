---
name: Bunch of Tips in Linux Bash
use_math: false
heading1: Bunch of Tips in Linux Bash
motivation: Someday it will all make sense.
about: SHELL
---

Bunch of Tips in Linux Bash

# Tips in Linux Bash

## Cryptography

### Verify the SHA256 sum of two package (such as 'a' and 'b')
```
sha256sum a # Get the SHA256 sum of 'a' package, then copy the SHA sum as "abcd"
diff <(echo "abcd") <(echo "the SHA256 gound truth of 'b' package")
```

## Matlab

### Create matlab entry in lauchpad of Ubuntu
```
sudo apt-get install matlab-support
```
### Install update
```
sudo bash /usr/local/MATLAB/R2019b/bin/glnxa64/update_installer
```