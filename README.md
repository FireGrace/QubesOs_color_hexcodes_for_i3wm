# QubesOs_color_hexcodes_for_i3wm
Some of the Colorcodes, based upon Qubes design documentation. Since the nature of i3wm, some changes were made.
https://www.qubes-os.org/doc/style-guide/


## Quik overview ##
* We take color codes from QubesOs style guide.
* Apply tint and shading where nessesary, to make in 3wm navigation easier
* Not using Qubes grayscale for fonts in i3 containers(windows)
* In favour of readability, we apply font colors, where they contrast more.

# Font color to color label #
Black fonts | White fonts
----------- | -----------
Green |  Red
Yellow | Blue
Orange | Purple
White(dom0) | Black
. | Gray

## Reasoning and explanations ##

Having the main idea of QubesOs extreme isolation, user ability to distinguish trust domains is crucial.
As the QubesOs have style guide, with explicit color codes, all Window Managers should follow it.

But, there is a catch. If we apply color codes as they are, we will make i3wm navigation extremly difficult.
And multimonitor setup, will make it event worse.

_The solution is to follow i3wm original rules of shading and tinting, using QubesOs spec colors as basis._

But this does not works really well with *Fonts*. Main black and Backgournd white that QubesOs presents in ints grayscale
have a little contrast when shown above color labels. In short, it's hard to read it

_The solution is to make exception to font colors, in context of i3wm containers(windows)_

Still we have issues with *dom0*. The xfce4 have the ability to change, dom0 interface colors easy.
And it comes to the user preference what is *should* be. I3wm presents the user the same ability to change
colors, but its harder to change for end user (hexcolors and config editing), comparing to xfce4 gui tools.
We have to make the default dom0 colors distinguishable from any other color. The free place is in grayscale.
Black and Gray are already in use.

_The solution is to use white colors from QubesOs grayscale, in order to make dom0 look different_

