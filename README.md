# Spotify BPM splitter

This is a toy Python app to split a [Spotify](https://www.spotify.com/) playlist in multiple children playlists sorted by tempo / BPM using the [Spotify web API](https://beta.developer.spotify.com/documentation/web-api/) through [`spotipy`](http://spotipy.readthedocs.io/en/latest/).

## Requirements
1. `pip install spotipy`
2. [Spotify credentials](https://developer.spotify.com/my-applications). More info in the [`spotipy` docs](http://spotipy.readthedocs.io/en/latest/#authorization-code-flow)

## Usage
Get the playlist [URI](https://en.wikipedia.org/wiki/Uniform_Resource_Identifier) by right-clicking on it on Spotify, go to `Share` and `Copy Spotify URI`. Pass it as an argument to the Python script:

```shell
$ JAZZ_URI="spotify:user:spotify:playlist:37i9dQZF1DWTR4ZOXTfd9K"
$ python splitter $JAZZ_URI
```

## Caveats
* You need to create a dummy Spotify app to get your authentication credentials
* The Spotify API doesn't seem to return more than 100 songs from a playlist
* Current bin size for the playlists is hard-coded to 10 BPM
* The script doesn't check if a playlist exists already when running it a second time

## Contributing
Contributions are welcome!
