### Stéganographie

## Fichier Audio 

+ Sonic visualizer
+ Audacity
+ ffmpeg 
    + Permet de checker l'intégrité d'un fichier audio et repoter les info et les erreurs

```console
ffmpeg -v info -i stego.mp3 -f null -
```
+ AdioStego
    + idem mais pour les fichier MP3/WAW
```console
hideme stego.mp3 -f && cat output.txt

FLAG{Steg01nmp3}
```

+mp3stego (Windows)
     + Outil permettant de cacher de la donnée dans un mp3 ou wav. Disponible sous Windows only (https://www.petitcolas.net/steganography/mp3stego/)
  ```console
Decode.exe -X Chall.wav -A

Input file = 'Chall.wav'  output file = 'Chall.wav.aif'
Output file written in AIFF format
Will attempt to extract hidden information. Output: Chall.wav.txt
Enter a passphrase:
the bit stream file Chall.wav is a BINARY file
Decoding of "Chall.wav" is finished
The decoded PCM output file name is "Chall.wav.aif"
"Chall.wav.aif" has been written with AIFF header information

type Chall.wav.txt

FLAG{GG_Y0u_W1n}
```
+ WavePad
    + Permet d'effectuer plusieurs transformations sur le son et ses fréquences (Un des plus simple d'utilisation) https://www.nch.com.au/wavepad/fr/index.html

+ QSSTV
    + Permet d'afficher le signal de transmission SSTV
```console
Configuration -> Audio Input -> From File -> signals.wav
```

## Fichiers Images
+ LSB-Steganographie
    + Outil permettant d'encoder/décoder de la data en modifiant les bits de couleur (LSB) Download Here ->https://github.com/RobinDavid/LSB-Steganography Utilisation :
```console
$python2 LSB-Steganography/LSBSteg.py decode -i chall.png -o flag && cat flag

flag{you_own_me}
```

+ exiftool
    + Affiche les meta-données EXIF d'un fichier
 ```console
$exiftool file.jpg

File Size                       : 120 kB
File Modification Date/Time     : 2018:03:09 22:08:42+01:00
Resolution Unit                 : inches
X Resolution                    : 96
Y Resolution                    : 96
XMP Toolkit                     : Image::ExifTool 10.63
Description                     : Tu es sur la bonne voie, continue !
Subject                         : Password
IPTC Digest                     : d41d8cd98f00b204e9800998ecf8427e
URL                             : aG9tZXIgc2ltcHNvbg==
....
 ```
 + Gimp / PhotoFiltre / Photoshop 
    + Jouer avec les contrastes, couleurs peut quelques fois s'avérer utile
 + Steghide
    + Permet de dissimuler du texte dans un fichier (image ou son)
 ```console 
 $steghide extract -sf ch10.jpg

Entrez la passphrase:
écriture des données extraites dans "password.txt"
  ```
