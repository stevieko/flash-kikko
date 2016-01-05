**Experiments and open source code for flash**

| ![http://kikko.fr/medias/250.jpg](http://kikko.fr/medias/250.jpg) | **List of current flash projects :**  |
|:------------------------------------------------------------------|:--------------------------------------|



---




# Shine MP3 Encoder on Alchemy <wiki:gadget url="http://stefansundin.com/stuff/flattr/google-project-hosting.xml" border="0" width="100" height="17" up\_button="compact" up\_uid="458" up\_title="AS3/Alchemy port Shine MP3 Encoder" up\_desc="Shine (formely 8hz-MP3) is a simple lightweight C-based MP3 encoder made by LAME developer Gabriel Bouvigne" up\_tags="as3,alchemy,mp3" up\_url="http://code.google.com/p/flash-kikko/#Shine\_MP3\_Encoder\_on\_Alchemy" /> #

## Description ##

Shine (formely 8hz-MP3) is a simple lightweight C-based MP3 encoder made by LAME developer [Gabriel Bouvigne](http://gabriel.mp3-tech.org/).

**Description of Shine on his website:**
> _The goal of this encoder was not quality, but simplicity. I tryed to simplify the encoding process as much as possible. So Shine is then a good starting point when a programmer needs a very simple MP3 encoder_

**This Alchemy port features:**
  * MP3 encoding of mono and stereo WAVs (no time limit)
  * non-blocking encoding for progress status in flash
  * errors automatically sent to flash for easy log/debug

_Also, thanks to Bernard Hilger Visscher for his very helpful blog post http://blog.debit.nl/?p=67_

## Usage ##
```
import fr.kikko.lab.ShineMP3Encoder;

private function encodeToMP3(wavData:ByteArray):void {
			
	mp3Encoder = new ShineMP3Encoder(wavData);
	mp3Encoder.addEventListener(Event.COMPLETE, mp3EncodeComplete);
	mp3Encoder.addEventListener(ProgressEvent.PROGRESS, mp3EncodeProgress);
	mp3Encoder.addEventListener(ErrorEvent.ERROR, mp3EncodeError);
	mp3Encoder.start();
}

private function mp3EncodeProgress(event : ProgressEvent) : void {
			
	trace(event.bytesLoaded, event.bytesTotal);
}

private function mp3EncodeError(event : ErrorEvent) : void {
			
	trace("Error : ", event.text);
}

private function mp3EncodeComplete(event : Event) : void {
			
	trace("Done !", mp3Encoder.mp3Data.length);
}
```

## Demo ##
&lt;wiki:gadget url="http://hosting.gmodules.com/ig/gadgets/file/115706021283080868825/shinemp3\_alchemy.xml" width="350" height="120" border="0"/&gt;

## Downloads ##

The project has moved to github : http://github.com/kikko/Shine-MP3-Encoder-on-AS3-Alchemy

Please note that original Shine libray is distributed under GPL License.

<wiki:gadget url="http://stefansundin.com/stuff/flattr/google-project-hosting.xml" border="0" width="66" height="76" up\_uid="458" up\_title="AS3/Alchemy port Shine MP3 Encoder" up\_desc="Shine (formely 8hz-MP3) is a simple lightweight C-based MP3 encoder made by LAME developer Gabriel Bouvigne" up\_tags="as3,alchemy,mp3" up\_url="http://code.google.com/p/flash-kikko/#Shine\_MP3\_Encoder\_on\_Alchemy" />