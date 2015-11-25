# analyser-average-frequency

[![stable](http://badges.github.io/stability-badges/dist/stable.svg)](http://github.com/badges/stability-badges)

For the given WebAudio [AnalyserNode](https://developer.mozilla.org/en/docs/Web/API/AnalyserNode), determine the average signal (0 .. 1) between two frequency ranges in Hz. This can be useful for audio visualization on a certain spectrum of the frequency graph.

The frequency is assumed to be in byte data, though you can use the `floatData` entry point to get around this.

## Usage

[![NPM](https://nodei.co/npm/analyser-average-frequency.png)](https://www.npmjs.com/package/analyser-average-frequency)

#### `avg = average(analyser, frequencies, minHz, maxHz)`

Returns the average signal in `0 .. 1` range for the given `analyser` (AnalyserNode) and `frequencies` (array of byte frequency data from that node). The `minHz` and `maxHz` is the frequency range to sum, in Herz.

#### `avg = average.floatData(analyser, floatFrequencies, minHz, maxHz)`

The same as above, but intended to be used with the result of `analyserNode.getFloatFrequencyData()`. 

## License

MIT, see [LICENSE.md](http://github.com/Jam3/analyser-average-frequency/blob/master/LICENSE.md) for details.
