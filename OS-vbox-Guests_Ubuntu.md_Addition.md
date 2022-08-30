# Installera Guest Additions på Ubuntu

## Varför?

För att vi vill kunna ändra storlek på vm fönstret valfritt och vill kunna klippa och klistra mellan vm och host.

## Öppna en terminal

1. Klicka Show All Applications

![show applications](vbox-ga-show_applications.png)

2. Klicka på Terminal

![terminal](vbox-ga-terminal.png)

## Uppdatera repository och ladda ner uppdateringar

1. Skriv in `sudo apt update`
2. Skriv in `sudo apt upgrade`
3. Välj ja på alla frågor `Y`

![update](vbox-ga-update.png)

## Installera build tools

1. Skriv in `sudo apt install build-essential dkms linux-headers-$(uname -r)`
2. Välj ja på alla frågor `Y`

![buildtools](vbox-ga-buildtools.png)

## Sätt i Guest Additions CD

1. Klicka Devices i virtualbox menyn

![update](vbox-ga-devices.png)

2. Välj `Insert Guest Additions CD image`

![Guest Additions CD](vbox-ga-insertga.png)

## Installera Guest Additions

1. I terminalen skriv `cd /media`
2. Skriv `ls`
3. Använd katalognamnet (förmodligen ditt användarnamn) ex `cd jim`
4. Skriv `cd VBox_GAs_6.1.36` (tab kompletering fungerar, så räcker med `V` + `tab`)
5. Skriv `sudo ./VBoxLinuxAdditions.run` (tab kompletering fungerar, så räcker med `VBoxL` + `tab`)

![Guest Additions install](vbox-ga-ga-install.png)

## Stäng av (när installationen är klar)

1. Klicka top menyn

![top meny](vbox-ga-topmenu.png)

2. Välj Power Off

![power off](vbox-ga-poweroff.png)

## Ta ur CDn

1. Klicka `[Optical Drive]`
2. Välj `Remove disc from virtual drive`

![Optical Drive](vbox-ga-opticaldrive.png)

## Ställ in klipp och klistra

1. Öppna settings för ditt vm

![settings](vbox-ga-settings.png)

2. Välj General
3. Välj Advanced
4. Ställ in `Shared Clipboard` som Bidirectional

![clipboard](vbox-ga-cutnpaste.png)

## Starta ditt vm och logga in och pröva ändra storleken på det

![resize](vbox-ga-resize.png)

