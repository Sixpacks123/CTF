### Stéganographie

## Fichier Audio 

+ Sonic visualizer
+ Audacity
+ ffmpeg 
    + Permet de checker l'intégrité d'un fichier audio et repoter les info et les erreurs

```console
ffmpeg -v info -i stego.mp3 -f null -

+ AdioStego
    + idem mais pour les fichier MP3/WAW
```console
hideme stego.mp3 -f && cat output.txt

FLAG{Steg01nmp3}
