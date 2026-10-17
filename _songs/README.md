Turn the song title into a slug by removing any "A", "An", "The", etc. from the
beginning, then using the typical slug transformation.

In this directory, add a Markdown file named with the slug + `.md`, with the
following front matter fields.
All but `title` are optional.

| Name | Description |
| --- | --- |
| `title` | Song title |
| `date` | Release date |
| `composer` | Primary composer |
| `description` | Mapping: `en` and `ja` for English and Japanese song descriptions, respectively, in Markdown. |
| `lyrics` | Mapping: Lyrics, in the same format as `description`. |
| `streaming` | Streaming service song IDs.  See below. |
| `youtube` | Music video on YouTube.  For songs without videos, use `streaming.youtube_music`.  Mapping: `v` is the video ID, `aspect_ratio` is the CSS aspect ratio. |

Where the IDs are for each streaming service:

| Name | URL template |
| --- | --- |
| `apple_music` | `http://music.apple.com/jp/song/$TITLE/$ID` or `/jp/album/$TITLE/$ALBUM_ID?i=$ID` |
| `spotify` | `https://open.spotify.com/track/$ID?...` |
| `youtube_music` | `https://music.youtube.com/watch?v=$ID&...` |

For long Markdown fields, use the block scalar format:

```yaml
lyrics:
  en: |
    Lorem ipsum dolor sit amet\
    Consectetur adipiscing elit\
    Sed do eiusmod tempor incididunt\
    Ut labore et dolore magna aliqua

    Ut enim ad minim veniam\
    Quis nostrud exercitation ullamco laboris\
    Nisi ut aliquip ex ea commodo consequat
  ja: |
    あのイーハトーヴォのすきとおった風\
    夏でも底に冷たさをもつ青いそら\
    うつくしい森で飾られたモリーオ市\
    郊外のぎらぎらひかる草の波

    またそのなかでいっしょになったたくさんのひとたち\
    ファゼーロとロザーロ\
    羊飼のミーロや
```

Add cover art as `cover.jpg` in a subdirectory named with the slug.
