# 2022-2023-project-5-algorithmics-Team-6

- [2022-2023-project-5-algorithmics-Team-6](#2022-2023-project-5-algorithmics-team-6)
  - [Overview](#overview)
  - [How to use it](#how-to-use-it)
  - [Documents](#documents)
  - [Team members](#team-members)
  - [Footnotes](#footnotes)


## Overview

This project aims to provide an algorithm to mix different still wines[^still_wines] into a tank, ultimately creating a specific kind of champagne.

## How to use it

The following steps require you to install the last version of the wine mixer program first.

### Windows

To access the program folder open the console and type:

```
cd Downloads/WineMixer
```

you can modify the inputs as you want inside the input folder, the inputs are:

- recipe.txt, which is the recipe you hope to achieve,
- tanks.txt, which is the tanks and their respective size.

To modify it type in the console:

```
notepad input/recipe.txt
```

or

```
notepad input/tanks.txt
```

Then to execute the program type:

```
WineMixer.exe
```

Finally, you can see the results on the terminal and inside the output folder created in the program's folder.

### Mac

To access the program folder open the console and type:

```
cd Downloads/WineMixer
```

you can modify the inputs as you want inside the input folder, the inputs are:

- recipe.txt, which is the recipe you hope to achieve,
- tanks.txt, which is the tanks and their respective size.

To modify it type in the console:

```
nano input/recipe.txt
```

or

```
nano input/tanks.txt
```

Then to execute the program type and open the resulting outputs:

```
sudo dotnet WineMixer.dll input/tanks.txt input/recipe.txt && open /usr/local/share/dotnet/output
```

## Documents

[Functionnal specifications](./Functional_Specifications.md)  
[Test plan](./TestPlan.md)

## Team members

[David CUAHONTE CUEVAS](https://github.com/DavidCC812)  
[Christopher DIGGINS](https://github.com/cdiggins)  
[Jason GROSSO](https://github.com/JasonGROSSO)  
[Aurélien FERNANDEZ](https://github.com/aurelienfernandez)

## Footnotes

[^still_wines]: It is a wine obtained by natural fermentation, it is the traditional wine, also referred as white, rosé, red wine or more rarely orange.
