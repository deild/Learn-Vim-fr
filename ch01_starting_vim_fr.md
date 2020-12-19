<!--
# Ch 01. Starting Vim
-->

# Ch 01. Démarrage de Vim

<!--
In this chapter, you will learn different ways to start Vim from the terminal. I highly recommend you use Vim from the terminal as you are typing along. I am currently using Vim 8.2. You should be fine if you use a lower version, but some commands might not be available.
-->
Dans ce chapitre, vous apprendrez différentes façons de lancer Vim depuis le terminal. Je vous recommande vivement d'utiliser Vim à partir du terminal pendant que vous tapez. J'utilise couramment Vim 8.2. Vous devriez vous en sortir si vous utilisez une version inférieure, mais certaines commandes pourraient ne pas être disponibles.
<!--
## Installing
-->

## Installation

<!--
I will not go through the detailed instruction how to install Vim (because there are many different distros out there). The good news is, most Unix computers should come with Vim installed. If not, most distros should have a way to install Vim.
-->
Je ne passerai pas en revue les instructions détaillées sur l'installation de Vim (parce qu'il y a beaucoup de distrubutions différentes). La bonne nouvelle, c'est que la plupart des ordinateurs Unix devraient être livrés avec Vim installé. Si ce n'est pas le cas, la plupart des distributions devraient avoir un moyen d'installer Vim.
<!--
For more download information, check out Vim's official download website:
-->
Pour plus d'informations sur le téléchargement, consultez le site officiel de téléchargement de Vim :
<!--
[https://www.vim.org/download.php](https://www.vim.org/download.php)
-->
[https://www.vim.org/download.php](https://www.vim.org/download.php)
<!--
Alternatively, you can also check out Vim's [official github repository](https://github.com/vim/vim).
-->
Vous pouvez également consulter [dépôt github officiel](https://github.com/vim/vim) de Vim.
<!--
## `vim`
-->

## `vim`

<!--
Now that you have Vim installed, run this from the terminal:
-->
Maintenant que vous avez installé Vim, exécutez ceci depuis le terminal :
<!--
```bash
vim
```
-->

```bash
vim
```

<!--
You should see an intro screen. This is the where you will be working on your file. Unlike most text editors and IDEs, Vim is a modal editor. If you want to type "Hello", you need to switch to Insert mode with `i`. Type: `ihello<Esc>`.
-->
Vous devriez voir un écran d'introduction. C'est là que vous allez travailler sur votre fichier. Contrairement à la plupart des éditeurs de texte et des IDE, Vim est un éditeur modal. Si vous voulez taper "Hello", vous devez passer en mode d'insertion avec `i`. Tapez : 'iHello<Esc>'.
<!--
## Exiting Vim
-->

## Quitter Vim

<!--
There are several ways to exit Vim. The most common one is to type:
-->
Il y a plusieurs façons de sortir de Vim. La plus courante est de taper :
<!--
```
:quit
```
-->

```vim
:quit
```

<!--
You can type `:q` for short. That command is a Command-line mode command (another one of Vim modes). If you type `:` in Normal mode, the cursor will move to the bottom of the screen where you can type some commands. You will learn about the Command-line mode later in chapter 15. If you are in Insert mode, typing `:` will literally produce the character ":" on the screen. In this case, you need to switch back to Normal mode. Type `<Esc>` to switch to Normal mode. By the way, you can also return to Normal mode from Command-line mode by pressing `<Esc>`. You will notice that you can "escape" out of several Vim modes back to Normal mode by pressing `<Esc>`.
-->
Vous pouvez taper `:q` pour faire court. Cette commande est une commande en mode ligne de commande (un autre des modes de Vim). Si vous tapez `:` en mode Normal, le curseur se déplacera vers le bas de l'écran où vous pourrez taper quelques commandes. Vous en saurez plus sur le mode ligne de commande plus loin dans le chapitre 15. Si vous êtes en mode Insertion, le fait de taper `:` produira littéralement le caractère ":" à l'écran. Dans ce cas, vous devez revenir en mode normal. Tapez `<Esc>` pour passer en mode Normal. Au fait, vous pouvez également revenir en mode Normal depuis le mode Ligne de commande en appuyant sur `<Esc>`. Vous remarquerez que vous pouvez "échapper" de plusieurs modes de Vim pour revenir au mode Normal en appuyant sur `<Esc>`.
<!--
To save your changes, type:
-->
Pour enregistrer vos modifications, tapez :
<!--
```
:write
```
-->

```vim
:write
```

<!--
You can also type `:w` for short. If this is a new file, you need to give it a name before you can save it. Let's name it `file.txt`. Run:
-->
Vous pouvez également taper `:w` pour faire court. S'il s'agit d'un nouveau fichier, vous devez lui donner un nom avant de pouvoir l'enregistrer. Nommons-le `fichier.txt`. Exécuter :
<!--
```
:w file.txt
```
-->

```vim
:w fichier.txt
```

<!--
To save and quit, you can combine the `:w` and `:q` commands:
-->
Pour sauvegarder et quitter, vous pouvez combiner les commandes `:w` et `:q` :
<!--
```
:wq
```
-->

```vim
:wq
```

<!--
To quit without saving any changes, add `!` after `:q` to force quit:
-->
Pour arrêter sans enregistrer de modifications, ajoutez `!` après `:q` pour forcer l'arrêt :
<!--
```
:q!
```
-->

```vim
:q!
```

<!--
There are other ways to exit Vim, but these are the ones you will use daily.
-->
Il existe d'autres moyens de sortir de Vim, mais ce sont ceux que vous utiliserez quotidiennement.
<!--
## Help
-->

## Aide

<!--
Throughout the book, I will refer you to various Vim help pages. You can access the help page by typing the following Command-line command:
-->
Tout au long du livre, je vous renvoie aux différentes pages d'aide de Vim. Vous pouvez accéder à la page d'aide en tapant la commande suivante en ligne de commande :
<!--
```
:help
```
-->

```vim
:help
```

<!--
Or `:h` for short. You can also pass the `:h` command the subject you want to learn as an argument. For example, to learn more about different ways to quit Vim, you can type:
-->
Ou `:h` pour faire court. Vous pouvez également passer en argument à la commande `:h` le sujet que vous voulez apprendre. Par exemple, pour en savoir plus sur les différentes façons de quitter Vim, vous pouvez taper :
<!--
```
:h write-quit
```
-->

```vim
:h write-quit
```

<!--
## Opening a File
-->

## Ouverture d'un fichier

<!--
From the terminal, to open `hello1.txt` file, run:
-->
Depuis le terminal, pour ouvrir le fichier `hello1.txt`, exécutez :
<!--
```bash
vim hello1.txt
```
-->

```bash
vim hello1.txt
```

<!--
You can also open multiple files at once:
-->
Vous pouvez également ouvrir plusieurs fichiers en même temps :
<!--
```bash
vim hello1.txt hello2.txt hello3.txt
```
-->

```bash
vim hello1.txt hello2.txt hello3.txt
```

<!--
Vim opens `hello1.txt`, `hello2.txt`, and `hello3.txt` in separate buffers. You will learn more about buffers in the next chapter.
-->
Vim ouvre `hello1.txt`, `hello2.txt`, et `hello3.txt` dans des tampons séparés. Vous en apprendrez plus sur les tampons dans le prochain chapitre.
<!--
## Arguments
-->

## Arguments

<!--
You can pass the `vim` terminal command with different flags and options.
-->
Vous pouvez passer la commande de terminal `vim` avec différents drapeaux et options.
<!--
To check the current Vim version, run:
-->
Pour vérifier la version actuelle de Vim, exécutez :
<!--
```bash
vim --version
```
-->

```bash
vim --version
```

<!--
This flag tells you the Vim version and all available features marked with either `+` or `.` Some of these features in this guide require certain features to be available. For example, you will explore Vim's command-line history in chapter 15 with the `:history` command. Your Vim needs to have `+cmdline_history` feature for the command to work.
-->
Ce drapeau vous indique la version de Vim et toutes les fonctionnalités disponibles marquées d'un `+` ou d'un `-`. Certaines de ces fonctionnalités dans ce guide nécessitent la disponibilité de certaines fonctions. Par exemple, vous explorerez l'historique de la ligne de commande de Vim au chapitre 15 avec la commande `:history`. Votre Vim doit avoir la fonction `+cmdline_history` pour que la commande fonctionne.
<!--
This may sound like a lot of work, but the popular Vim downloads should have all the necessary features. In my Mac, the Vim version that I installed from `brew install vim` has all the features I need.
-->
Cela peut sembler beaucoup de travail, mais les téléchargements populaires de Vim devraient avoir toutes les caractéristiques nécessaires. Dans mon Mac, la version de Vim que j'ai installée à partir de `brew install vim` a toutes les fonctionnalités dont j'ai besoin.
<!--
Alternatively, to see the version information from *inside* Vim, you can also run this command:
-->
Alternativement, pour voir les informations de version *intérieur* de Vim, vous pouvez également exécuter cette commande :
<!--
```
:version
```
-->

```vim
:version
```

<!--
Later on, you will probably start adding plugins to Vim. If you ever need to run Vim without any plugins, you can pass the `noplugin` flag:
-->
Plus tard, vous commencerez probablement à ajouter des plugins à Vim. Si jamais vous avez besoin de faire tourner Vim sans aucun plugin, vous pouvez passer le drapeau `noplugin` :
<!--
```
vim --noplugin
```
-->

```bash
vim --noplugin
```

<!--
If you want to open the file `hello.txt` and immediately execute a command, you can pass the `vim` command the `+{cmd}` option.
-->
Si vous voulez ouvrir le fichier `hello.txt` et exécuter immédiatement une commande, vous pouvez passer à la commande `vim` l'option `+{cmd}`.
<!--
In Vim, you can substitute text with the `:s` command (short for `:substitute`). If you want to open `hello.txt` and substitute all "foo" with "bar", run:
-->
Dans Vim, vous pouvez remplacer le texte par la commande `:s` (abréviation de `:substitute`). Si vous voulez ouvrir `hello.txt` et remplacer tous les "foo" par "bar", exécutez :
<!--
```bash
vim +%s/foo/bar/g hello.txt
```
-->

```bash
vim +%s/foo/bar/g hello.txt
```

<!--
These commands can also be stacked:
-->
Ces commandes peuvent également être empilées :
<!--
```bash
vim +%s/foo/bar/g +%s/bar/baz/g +%s/baz/donut/g hello.txt
```
-->

```bash
vim +%s/foo/bar/g +%s/bar/baz/g +%s/baz/donut/g hello.txt
```

<!--
Vim will first replace all instances of "foo" with "bar", then replace "bar" with "baz", then replace "baz" with "donut" (you willl learn about substitution in chapter 12).
-->
Vim va d'abord remplacer toutes les occurrences de "foo" par "bar", puis remplacer "bar" par "baz", puis remplacer "baz" par "donut" (vous en saurez plus sur la substitution au chapitre 12).
<!--
You can also pass the `c` flag followed by the command instead of the `+` syntax:
-->
Vous pouvez également passer le drapeau `c` suivi de la commande au lieu de la syntaxe `+` :
<!--
```bash
vim -c %s/foo/bar/g hello.txt
vim -c %s/foo/bar/g -c %s/bar/baz/g -c %s/baz/donut/g hello.txt
```
-->

```bash
vim -c %s/foo/bar/g hello.txt
vim -c %s/foo/bar/g -c %s/bar/baz/g -c %s/baz/donut/g hello.txt
```

<!--
Throughout this book you will learn various Command-line commands. These commands can all be executed on start.
-->
Tout au long de ce livre, vous apprendrez les différentes commandes de la ligne de commande. Ces commandes peuvent toutes être exécutées au démarrage.
<!--
## Opening Multiple Windows
-->

## Ouvrir des fenêtres multiples

<!--
You can launch Vim on split windows, horizontal and vertical, with `o` and `O`, respectively.
-->
Vous pouvez lancer Vim sur des fenêtres divisées, horizontales et verticales, avec respectivement un `o` et un `O`.
<!--
To open Vim with two horizontal windows, run:
-->
Pour ouvrir Vim avec deux fenêtres horizontales, exécutez :
<!--
```bash
vim -o
```
-->

```bash
vim -o
```

<!--
To open Vim with 5 horizontal windows, run:
-->
Pour ouvrir Vim avec 5 fenêtres horizontales, exécutez :
<!--
```bash
vim -o5
```
-->

```bash
vim -o5
```

<!--
To open Vim with 5 horizontal windows and fill up the first two with `hello1.txt` and `hello2.txt`, run:
-->
Pour ouvrir Vim avec 5 fenêtres horizontales et remplir les deux premières avec `hello1.txt` et `hello2.txt`, exécutez :
<!--
```bash
vim -o5 hello1.txt hello2.txt
```
-->

```bash
vim -o5 hello1.txt hello2.txt
```

<!--
Retrospectively, to open Vim with two vertical windows, 5 vertical windows, and 5 vertical windows with 2 files:
-->
Rétrospectivement, pour ouvrir Vim avec deux fenêtres verticales, 5 fenêtres verticales, et 5 fenêtres verticales avec 2 fichiers :
<!--
```bash
vim -O
vim -O5
vim -O5 hello1.txt hello2.txt
```
-->

```bash
vim -O
vim -O5
vim -O5 hello1.txt hello2.txt
```

<!--
## Suspending
-->

## Suspension

<!--
If you need to suspend Vim while in the middle of editing, you can press `Ctrl-z`. Alternatively, you can also run either the `:stop` or `:suspend` command.
-->
Si vous devez suspendre Vim en plein milieu du montage, vous pouvez appuyer sur `Ctrl-z`. Vous pouvez aussi lancer la commande `:stop` ou `:suspend`.
<!--
To return to the suspended Vim, run `fg` from the terminal.
-->
Pour retourner au Vim suspendu, il faut exécuter `fg` depuis le terminal.
<!--
## Starting Vim The Smart Way
-->

## Démarrage de Vim de maniére intelligente

<!--
You can pass the `vim` command with different options and flags, just like any terminal commands. One of the options is the command-line command (`+{cmd}` or `c cmd`). As you learn more command-line commands throughout this book, see if you can apply it on start.
-->
Vous pouvez passer la commande `vim` avec différentes options et drapeaux, comme pour toute commande de terminal. L'une des options est la commande en ligne de commande (`+{cmd}` ou `c cmd`). Au fur et à mesure que vous apprenez d'autres commandes en ligne de commande dans ce livre, voyez si vous pouvez l'appliquer au démarrage.
<!--
To learn more about the different options you can pass from the terminal, check out `man vim`. To learn more about Vim modes and commands, check out `:help`.
-->
Pour en savoir plus sur les différentes options que vous pouvez passer depuis le terminal, consultez `man vim`. Pour en savoir plus sur les modes et les commandes de Vim, consultez la page `:help`.
