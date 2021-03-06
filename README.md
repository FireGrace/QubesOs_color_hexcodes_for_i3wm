# QubesOs_color_hexcodes_for_i3wm
Some of the Colorcodes, based upon Qubes design documentation. Since the nature of i3wm, some changes were made.
[QubesOs Style guide](https://www.qubes-os.org/doc/style-guide/)


## Quik overview ##
* We take color codes from QubesOs style guide.
* Apply tint and shading where nessesary, to make in 3wm navigation easier
* Not using Qubes grayscale for fonts in i3 containers(windows)
* For indicator color we use complementary one to background. It changes with states too.
* In favour of readability, we apply font colors, where they contrast more.

# Font color to color label #
Black fonts | White fonts
----------- | -----------
Green |  Red
Yellow | Blue
Orange | Purple
White(dom0) | Black
. | Gray

**Qubes grayscale Fonts are applied to dmenu and i3 bar, since the contrast there is not the issue**


## Reasoning and explanations ##

Having the main idea of QubesOs extreme isolation, user ability to distinguish trust domains is crucial.
As the QubesOs have style guide, with explicit color codes, all Window Managers should follow it.

But, there is a catch. If we apply color codes as they are, we will make i3wm navigation extremly difficult.
And multimonitor setup, will make it event worse.

__The solution is to follow i3wm original rules of shading and tinting, using QubesOs spec colors as basis.__

But this does not works really well with *Fonts*. Main black and Backgournd white that QubesOs presents in ints grayscale
have a little contrast when shown above color labels. In short, it's hard to read it

__The solution is to make exception to font colors, in context of i3wm containers(windows)__

Still we have issues with *dom0*. The xfce4 have the ability to change, dom0 interface colors easy.
And it comes to the user preference what is *should* be. I3wm presents the user the same ability to change
colors, but its harder to change for end user (hexcolors and config editing), comparing to xfce4 gui tools.
We have to make the default dom0 colors distinguishable from any other color. The free place is in grayscale.
Black and Gray are already in use.

__The solution is to use white colors from QubesOs grayscale, in order to make dom0 look different__

3iwm have interesting feature, of indication where the window will be opened. It activates when you create a split container.
Unfortunately we have many colors to draw, and indicator will be unseen with some color, no matter what we choose.
So no one solid color will fix the issue. The most we can do, is to make indicator contrast with container(windows) colors.

__The solutions is to use complementary colors for each state the windows is in.__
__Other way is to ask i3wm devs to implement different drawing system for indicators, where they will appear as dotted line,
drawn upon background color. Or path this in Qubes repo.__
