# Promotional Kirby Contest Card (Loser) Disassembly

> E3 2002 promotional Kirby e-Reader cards were distributed on the E3 showfloor. Each card was printed in 3 variants - no prize, 2nd prize, and 1st prize. Scanning the card would result in confirmation if you've won a prize or not. All winning cards were later destroyed.
[@FactsKirby](https://twitter.com/FactsKirby/status/1100787610769915904)

See [this card's entry in the e-Reader Encyclopedia](http://ereader.no-intro.org/checklists.php?sys=EngList&search_set=Promotional&card_no=1152).

![ ](img/card.png)

![ ](img/screenshot.png)

## How to build

* Download [SDCC](http://sdcc.sourceforge.net/)
* Download e-reader tools from [caitsith2.com](https://www.caitsith2.com/ereader/index.htm)

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

### Background
![ ](img/bg0.png)

### Sprites
![ ](img/tiles.png)
