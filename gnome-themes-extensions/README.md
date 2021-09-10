# How to install themes and extensions on GNOME at 42Paris

Contrary to MacOS or Windows, Linux is fully customizable. You can install user themes for your applications or the icons set, and extensions to add features to your desktop.

## Themes

There are plenty ways to search and download themes, but I am going to show you one. The website I am going to use is [https://gnome-look.org](https://gnome-look.org).

I recommend you downloading from **Gnome-Look** so that the repository containing the theme won't be deleted from the website.

### Applications

> For this example, we are going to use the Marwaita theme.
> [GitHub](https://github.com/darkomarko42/Marwaita) - [Gnome-Look](https://www.gnome-look.org/p/1239855)

Download the repository and unzip it.

```shell
$ unzip Marwaita-master.zip
$ cd Marwaita-master
$ ls
 LICENSE   'Marwaita Alternative'       'Marwaita Color'       'Marwaita Dark'
 Marwaita  'Marwaita Alternative Dark'  'Marwaita Color Dark'   README.md
```

You can see that there are some alternatives to the theme, whether you want it light or dark. Let's choose **Marwaita** (classic).

In order to detect the theme, it has to be copied in a specific folder, which is `$HOME/.themes` (create the folder if it doesn't exist).

```shell
$ mkdir -p ~/.themes
$ cp -r Marwaita ~/.themes
```

Now, you will be able to set the desired theme in the **Tweaks** application (Appearance > Themes > Applications).

You can also set it using the following command.

```shell
$ gsettings set org.gnome.desktop.interface gtk-theme "Marwaita"
```

#### Help for the future

You won't always download themes that has the same file hierarchy as **Marwaita**. The most important thing to remember is that the folder that you need to copy always contains a file called `index.html` at its root.

### Icons

> For this example, we are going to use the Luna Icons set.
> [GitHub](https://github.com/darkomarko42/Luna-Icons) - [Gnome-Look](https://www.gnome-look.org/p/1405455)

Download the repository and unzip it.

```shell
$ unzip Luna-Icons-master.zip
$ cd Luna-Icons-master
$ ls
 LICENSE   Luna-Dark        'Luna icons OSX Dark'    Luna-Light
 Luna     'Luna icons OSX'  'Luna icons OSX Light'   README.md
```

You can see that there are some alternatives to the theme, whether you want it light or dark. Let's choose **Luna** (classic).

In order to detect the set, it has to be copied in a specific folder, which is `$HOME/.icons` (create the folder if it doesn't exist).

```shell
$ mkdir -p ~/.icons
$ cp -r Luna ~/.icons
```

Now, you will be able to set the desired set in the **Tweaks** application (Appearance > Themes > Icons).

You can also set it using the following command.

```shell
$ gsettings set org.gnome.desktop.interface icon-theme "Luna"
```
