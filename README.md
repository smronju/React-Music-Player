React Music Player
=====================

A simple HTML5 music player with ReactJS and CSS3.  
[Modified version of react-cl-audio-player](https://github.com/CezarLuiz0/react-cl-audio-player)


### To see the examples locally, run:

```
npm install
npm run example
```

Then open [`localhost:8080`](http://localhost:8080/webpack-dev-server/) in a browser.

## Installation

The easiest way to use react-music-player-player is to install it from NPM and include it in your own React build process (using [Browserify](http://browserify.org), [Webpack](http://webpack.github.io/), etc).

You can also use the standalone build by including `dist/ReactMusicPlayer.js` in your page. If you use this, make sure you have already included React, and it is available as a global variable.

```
npm install react-music-player --save
```

### Usage

To use, just call the ReactMusicPlayer instance and render it.

```
import ReactMusicPlayer from 'react-music-player';
<ReactMusicPlayer songs={songs} autoplay />
```

### Properties

* songs - An array with the object songs - required
* songs[0].url - string
* songs[0].cover - string - optional
* songs[0].artist - object
* songs[0].artist.name - string
* songs[0].artist.song - string
* autoplay - Is autoplay?

#### Songs model:

```
var songs = [
  {
    url: 'path/to/mp3',
    cover: 'path/to/jpeg',
    artist: {
      name: 'Metallica',
      song: 'Fuel'
    }
  },
  {
    url: 'path/to/your/mp3',
    artist: {
      name: 'X Japan',
      song: 'Art of Life'
    }
  }
];

```

#### CSS classes
* .no-height - A helper class for songs without covers
* .player-container
* .player-cover
* .artist-info
* .artist-name
* .artist-song-name
* .player-progress-container
* .player-progress-value
* .player-options
* .player-buttons
* .player-btn
* .player-btn i (.fa .fa-play .fa-pause .fa-volume .fa-volume-off .fa-forward .fa-backward .fa-repeat .fa-random)
* .player-btn.big.medium.small.active.volume:disabled
* .player-controls



### Notes

Works perfectly in Chrome, Firefox and Safari. No test in IE.


## Development (`src` and the build process)

**NOTE:** The source code for the component is in `src`. A UMD bundle is also built to `dist`, which can be included without the need for any build system.

To build and serve the examples, run `npm run build`, `npm run example`.

## License

MIT License.

Copyright (c) 2015 smronju.
