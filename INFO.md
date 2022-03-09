Since RCNES (ReCompiled Nintendo Entertainment System) is just a theory at the moment, here is info on that theory:

# The Idea
Simply put, what if we converted:

```assembly
ld x, y
```

into

```c
LoadRegister(X, GetYRegisterValue()); // ld x, y
```

This way, we have a true **port** of any NES game.
Now onto handling assets.
Basically, an RCNES game will be structured like this:

```
Super Mario Bros. (U).nes
Super Mario Bros. (U).exe
rcnes
    |
    Super Mario Bros. (U).ast
    Super Mario Bros. (U).asm
    Super Mario Bros. (U).sav
```

The `.ast` file holds assets from CHR-ROM/RAM
The `.asm` file holds program data from PRG-ROM/RAM
The `.sav` file (is somewhat rare and) holds save data 

