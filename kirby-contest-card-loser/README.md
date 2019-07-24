# Kirby Contest Card - Loser

![card](img/card.png)

![screenshot](img/screenshot.png)

## How to build

* Download SDCC
* Download e-reader tools

Compile:
```
sdasz80.exe -l -o -s -p main.o main.asm
```

Link:
```
sdldz80.exe -n -- -i main.ihx main.o
```

Make binary:
```
makebin.exe -p < main.ihx > main.z80
```

Remove first 256 bytes of `main.z80`.

Generate `RAW`:
```
nedcmake.exe -i main.bin -o us -type 1 -region 1
```

## Assets

** Background **
![bg0](img/bg0.png)

![tiles](img/tiles.png)