WaveHeader
====

Just generates a WAVE-file header, with the specified length as argument.

```javascript
var header = require("waveheader");
//write to a normal fs.createWriteStream
myFileStream.write(header(44100 * 8)); // 44100 khz * 8 seconds


// using options (all available options listed)
myOtherFileStream.write(header(22050 * 8) {
  sampleRate: 22050,
  channels: 2,
  bitDepth: 8
}); 
```

### Use with tonegenerator:
Also check out the module for generating tones as raw PCM data,
[tonegenerator](http://npmjs.com/package/tonegenerator).

### using the debug module

Waveheader uses the 'debug' module to clean the output a bit. If running your program from the command line, and you wanna see the size written to the header, do `DEBUG=waveheader node yourprogram.js`
