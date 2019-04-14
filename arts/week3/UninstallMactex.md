# Uninstall Mactex

Mactex is the latex distribution texlive's edition on MacOS platform. It is easy to install, just dowbload its image and after several clicks and several minutes' waiting, you can enjoy latex.



But when you're tired with mactex or you want to upgrade to a newer version, the process of uninstalling it is annoying. Following [steps on official sites](http://www.tug.org/mactex/uninstalling.html) , the first 3 steps are wasy to handle. For the last step, we could follow:

We need a complete image from, say [tuna](https://mirrors.tuna.tsinghua.edu.cn/CTAN/systems/mac/mactex/).

```bash
wget https://gist.githubusercontent.com/gwerbin/dcba755b0484423e9e45/raw/f46b24273ec03e81efe3b0c5c674dc7b22bdc064/uninstall-ghostscript.sh`

./uninstall-ghostscript.sh mactex-20180417.pkg
# Other versions are OK.
```

