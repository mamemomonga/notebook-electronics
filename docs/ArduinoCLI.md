# ArduinoCLI

# [MiniCore](https://github.com/MCUdude/MiniCore)

Device                                                    | FQBN
----------------------------------------------------------|----------------------------
ATmega168                                                 | MiniCore:avr:168
ATmega328                                                 | MiniCore:avr:328
ATmega48                                                  | MiniCore:avr:48
ATmega8                                                   | MiniCore:avr:8
ATmega88                                                  | MiniCore:avr:88

# [MegaTinyCore](https://github.com/SpenceKonde/megaTinyCore)

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

