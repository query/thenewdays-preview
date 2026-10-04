Turn the song title into a slug by removing any "A", "An", "The", etc. from the
beginning, then using the typical slug transformation.

Use the following layout for song directories:

| File | Content |
| --- | --- |
| Slug + `.md` | Metadata in front matter; see below |
| `_lyrics_en.md` | Original English lyrics |
| `_lyrics_ja.md` | Japanese translation of previous |

Put the cover in the root `covers` directory, named with the slug + `.jpg`.

Front matter fields:

| Name | Description |
| --- | --- |
| `title` | Song title |
| `date` | Release date |
| `youtube` | (Optional) Mapping: `v` is the video ID, `aspect_ratio` is the CSS aspect ratio. |
