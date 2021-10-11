# ArduinoCLI

# [MiniCore](https://github.com/MCUdude/MiniCore)

Device                                                    | FQBN
----------------------------------------------------------|----------------------------
ATmega168                                                 | MiniCore:avr:168
ATmega328                                                 | MiniCore:avr:328
ATmega48                                                  | MiniCore:avr:48
ATmega8                                                   | MiniCore:avr:8
ATmega88                                                  | MiniCore:avr:88

# [MegaCoreX](https://github.com/MCUdude/MegaCoreX)

Device                                                    | FQBN
----------------------------------------------------------|----------------------------
ATmega1608                                                | MegaCoreX:megaavr:1608
ATmega1609                                                | MegaCoreX:megaavr:1609
ATmega3208                                                | MegaCoreX:megaavr:3208
ATmega3209                                                | MegaCoreX:megaavr:3209
ATmega4808                                                | MegaCoreX:megaavr:4808
ATmega4809                                                | MegaCoreX:megaavr:4809
ATmega808                                                 | MegaCoreX:megaavr:808
ATmega809                                                 | MegaCoreX:megaavr:809

# [MegaTinyCore](https://github.com/SpenceKonde/megaTinyCore)

### [48-pin Standard: ATmega809, ATmega1609, ATmega3209, ATmega4809](https://camo.githubusercontent.com/4a630fb15a200b964cfd6e3f2ab46130a033774ba04d8c421ff1c2248c64af10/68747470733a2f2f692e696d6775722e636f6d2f335055424236482e6a7067)

### [UNO WifFi Rev2: ATmega809, ATmega1609, ATmega3209, ATmega4809](https://camo.githubusercontent.com/a26d92dab91615df49f1cc227ffedda144b15c52578097295b6a53bd2f59976c/68747470733a2f2f692e696d6775722e636f6d2f51624f4f4f54642e706e67)

### [32-pin Standard: ATmega808, ATmega1608, ATmega3208, ATmega4808](https://camo.githubusercontent.com/f3f0293a5cffab15523ad96c41d5348a891e0799c66b842c8093a173bc6b506b/68747470733a2f2f692e696d6775722e636f6d2f32596c6d4538702e706e67)

### [28-pin standard: ATmega808, ATmega1608, ATmega3208, ATmega4808](https://camo.githubusercontent.com/f3943d878fe9116cc8e0224e11b55114b3d3534a0005f2d2a80153a7788840c5/68747470733a2f2f692e696d6775722e636f6d2f7a5879577669312e706e67)

### [DIP-40 standard: ATmega4809](https://camo.githubusercontent.com/28e21db0c2a93ac875b4119dc0afaf9fc2c4814f42c1f6fc734bb8bf7be986a4/68747470733a2f2f692e696d6775722e636f6d2f4870323153584a2e6a7067)


	 TXD1    D8  PC0 | 1    40 | PA7 D7       SS
	 RXD1    D9  PC1 | 2    39 | PA6 D6       SCK
	         D10 PC2 | 3    38 | PA5 D5       MISO
	         D11 PC3 | 4    37 | PA4 D4       MOSI
	             VCC | 5    36 | PA3 D3       SCL
	             GND | 6    35 | PA2 D2       SDA
	         D12 PC4 | 7    34 | PA1 D1       RXD0
	         D13 PC5 | 8    33 | PA0 D0       TXD0
	      D14/A0 PD0 | 9    32 | GND
	      D15/A1 PD1 | 10   31 | VCC
	      D16/A2 PD2 | 11   30 | UPDI
	      D17/A3 PD3 | 12   29 | 
	      D18/A4 PD4 | 13   28 | PF5 D31/A15
	      D19/A5 PD5 | 14   27 | PF4 D30/A14
	      D20/A6 PD6 | 15   26 | PF3 D29/A13
	      D21/A7 PD7 | 16   25 | PF2 D28/A12
	            AVCC | 17   24 | PF1 D27      RXD2
	             GND | 18   23 | PF0 D26      TXD2
	      D22/A8 PE0 | 19   22 | PE3 D25/A11
	      D23/A0 PE1 | 20   21 | PE2 D24/A10

ATmega4809, DIP-40, OptiBootなし, 内部20MHz

	$ arduino-cli upload -b MegaCoreX:megaavr:4809:pinout=40pin_standard,clock=internal_20MHz -p /dev/cu.usbserial-0001 -P jtag2updi 

Device                                                    | FQBN
----------------------------------------------------------|----------------------------
ATtiny1614/1604/814/804/414/404 w/Optiboot                | megaTinyCore:megaavr:atxy4o
ATtiny3216/1616/1606/816/806/416/406 w/Optiboot           | megaTinyCore:megaavr:atxy6o
ATtiny3217/1617/1607/817/807/417 w/Optiboot               | megaTinyCore:megaavr:atxy7o
ATtiny3224/1624/1614/1604/824/814/804/424/414/404/214/204 | megaTinyCore:megaavr:atxy4
ATtiny3224/1624/824/424 w/Optiboot                        | megaTinyCore:megaavr:atx24o
ATtiny3226/1627/826/426 w/Optiboot                        | megaTinyCore:megaavr:atx26o
ATtiny3226/3216/1626/1616/1606/826/816/806/426/416/406    | megaTinyCore:megaavr:atxy6
ATtiny3227/1627/827/427 w/Optiboot                        | megaTinyCore:megaavr:atx27o
ATtiny3227/3217/1627/1617/1607/827/817/807/427/417        | megaTinyCore:megaavr:atxy7
ATtiny412/402/212/202                                     | megaTinyCore:megaavr:atxy2
ATtiny412/402/212/202 w/Optiboot                          | megaTinyCore:megaavr:atxy2o

## [ATtiny 406/806/1606](https://github.com/SpenceKonde/megaTinyCore/blob/master/megaavr/extras/ATtiny_x06.md)

            VCC  | 1    20 |  GND
    SS  D0  PA4  | 2    19 |  PA3  D16  SCK
        D1  PA5  | 3    18 |  PA2  D15  MISO
        D2  PA6  | 4    17 |  PA1  D14  MOSI
        D3  PA7  | 5    16 |  UPDI
        D4  PB5  | 6    15 |  PC3  D13
        D5  PB4  | 7    14 |  PC2  D12
    RXD D6  PB3  | 8    13 |  PC1  D11
    TXD D7  PB2  | 9    12 |  PC0  D10
    SDA D8  PB1  | 10   11 |  PB0  D9  SCL 

### ATTiny1606, OptiBootなし, 内部20MHz, jtag2updi

詳細情報の表示

    $ arduino-cli board details --fqbn=megaTinyCore:megaavr:atxy6

コンパイルとアップロード

    $ arduino-cli compile --fqbn=megaTinyCore:megaavr:atxy6:chip=1606,clock=20internal,startuptime=64 ./example
    $ arduino-cli upload -P jtag2updi -p /dev/cu.usbserial-2001 --fqbn=megaTinyCore:megaavr:atxy6:chip=1606,clock=20internal,startuptime=64 ./example

# Makefileサンプル

    AR_PORT=/dev/cu.usbserial-0001
    AR_SKETCH=$(notdir $(basename $(shell find . -name '*.ino')))
    AR_FQBN=arduino:avr:uno

    upload: build/$(AR_SKETCH).ino.hex
        arduino-cli upload -b $(AR_FQBN) -p $(AR_PORT) --input-dir "$(CURDIR)/build"

    compile: build/$(AR_SKETCH).ino.hex

    serial:
        screen $(AR_PORT)

    clean:
        rm -rf build

    build/$(AR_SKETCH).ino.hex: $(AR_SKETCH)/$(AR_SKETCH).ino
        arduino-cli compile -b $(AR_FQBN) --build-path "$(CURDIR)/build" $(AR_SKETCH)

    .PHONY: upload compile serial clean

