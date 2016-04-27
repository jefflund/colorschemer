colorschemer
============

There are a number of Vim plugins which convert a gui-only colorscheme to be
useable with the terminal. This plugin does the opposite. This is certainly a
less common use case, but if you happen to use a 256 color only colorscheme
(such as the Lucid colorscheme provided with colorschemer), then this plugin
will make gvim much more usable. In particular, I was annoyed with the amount
of manual effort to keep the gui attributes in sync with the constantly
evolving cterm attributes in my own Lucid colorscheme. With this plugin, you
only have to maintain the cterm attributes, and colorschemer will automatically
convert that colorscheme to have the appropriate gui attributes when you use
gvim.

Assuming you use vundle (which you should), you can install colorschemer by
adding ```Plugin 'jlund3/colorschemer'``` to your vimrc and running
```:PluginInstall```. Other package managers will be similar. Once installed,
if you run gvim and have a colorscheme loaded, then colorschemer will
automatically convert every cterm highlight attribute into the appropriate gui
attribute.

If you want to check out the Lucid colorscheme, you can use ```colo lucid``` to
enable it. It is based on Lucius, and (at least to my eye) is quite pleasing.

Note that colorschemer requires that Vim be compiled with Python support. You
can check this with ```:echo has('python')```.
