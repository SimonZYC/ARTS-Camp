# Alternative latex on MacOS

Recently I really hate Mactex because it is difficult to uninstall and pollutes my enviromemt.

I googled and came up with 3 alternative ways.

## Miklatex

[Official site](https://miktex.org/)

This is another latex distribution maintained by Christian Schenk. It supports Windows, MacOS

and Linux. The biggest advantage is that It can automatically download packages needed to 

compile the program. Besides, it is easy to uninstall. The drawback is that it has few mirrors

And packages than CTAN's texlive.

## Tinytex

[Official Site](https://yihui.name/tinytex/)

Tinytex, based on texlive, is developed by Yihui Xie. It works best for R users but others can also

use it. It is light-weight and easy to manage.

After installing it following steps on its official website, I executed:

`tlmgr install scheme-full`

Then it downloaded all the packages, just like texlive-full. Although this is not consistent with the

author's preliminary purpose, this could save me much from installing lacking packages.

### Latex on Docker

Search latex in docker hub: [search](https://hub.docker.com/search?q=latex&type=image) and find anyone you like.

I have tried [bland/latex-docker](https://github.com/blang/latex-docker) and it worked. You can build your own image and delete it easily.