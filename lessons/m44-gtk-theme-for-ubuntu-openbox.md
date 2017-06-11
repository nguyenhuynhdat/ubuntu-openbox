---
layout: default
title: GTK THEME
description: install and configure a GTK theme.
---

GTK themes will define the appearance of applications on your system: the interfaces, the color of the taskbar (lxpanel only, tint2 will use its own configuration), the backgrounds for windows and tabs, the looks of GTK applications.

As oppose to Openbox theme which defines the **OUTSIDE** - the title and the windows border, an GTK theme defines the look of what are **INSIDE** that windows border.

+ Normal GTK+ apps (Firefox, Transmission, Geany...)

One of the things you should consider when install a theme is that which theme engines are needed. The creator of the theme often will tell you which theme engines will go with it.

**Install a GTK theme:**

Once you have downloaded a theme, place it into either of these directories: **~/.themes** or **/usr/share/themes**.

Let me illustrate with my system. We will install **FlatStudioGray** theme and you can download it here:

[http://gnome-look.org/content/show.php/FlatStudio?content=154296](http://gnome-look.org/content/show.php/FlatStudio?content=154296)

Extract the downloaded package.

Then, move extracted **Flatstudio** theme folder into **~/.theme** folder.

 In Linux, every file/folder with its name begin with a period (.) is hidden.The **".theme"** folder is often hidden and we need to unhide it: Using Thunar > View > Check “Show Hidden File”.

![terminator]({{site.baseurl}}/images/Terminal_split.jpg)

Now you can see ~/.theme folder and move Flatstudio folder to it.

As I have said, you need theme engines to make the theme look exactly like it supposes to. As with this theme, the author have instructed us to install **unico-engine** & **gtk2-engines-murrine**.

```
sudo apt-get install unico-engine gtk2-engines-murrine
````
Open **Lxappearance** (by the command **lxappearance**) > Under the **Widget** tab, choose **Flatstudio**.

And Voila! All should look good now.
