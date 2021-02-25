# Gazpacho
The saltiest pineapple in the peninusula.
```bash 
los=(
03:04 03:17 DespiertaDormilon
03:34 03:19 DTanTemprano
03:57 04:03 NoVayasTanDeprisa
05:30 05:34 QueComer
05:42 05:47 EsteBultoTanPesado
05:51 05:56 ManoMagicaPincho
06:19 06:25 Hierbas
07:23 07:27 NoTrabajoNoComes
07:26 07:29 HuirDeLosProblemas
07:31 07:35 NoSeasTanVago
07:34 07:44 YSobreTodoNoHacerNada
17:37 17:42 YoSoyGazpacho )
youtube-dl -f 251 https://youtu.be/aC2HTSggXN8
youtube-dl -F https://youtu.be/aC2HTSggXN8
mkdir LosFrutisAudios
cp Los\ Fruittis\ _\ La\ Primavera\ todo\ Altera\ _\ Serie\ de\ Animación\ Infantil-aC2HTSggXN8.webm  FrutisAudio.webm
for (( frutis=0; frutis<=35; frutis=frutis+3 ))
do
	ffmpeg -i FrutisAudio.webm -ss 00:${los[$frutis]} -to 00:${los[$(($frutis+1))]} ./LosFrutisAudios/${los[$(($frutis+2))]}.mp3
done
echo "Tot bé !"
```
