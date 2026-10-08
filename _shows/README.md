Front matter fields.
All but `date`, `venue`, and `location` are optional.

| Name | Description |
| --- | --- |
| `date` | Show date in ISO 8601 format. |
| `show_url` | URL of the venue schedule page, Instagram post, etc. for this specific show. |
| `venue` | Venue name. |
| `venue_url` | URL of the venue's Web site, Instagram, etc. |
| `location` | Mapping with `en` and `ja` keys for the English and Japanese names, respectively, of the venue's location. |
| `event_name` | Name of the specific event. |
| `times` | Mapping: `open`, `start`, `stage` (The New Days' stage time). |
| `tickets` | List of mappings: `en` and `ja` ticket type descriptions; `price` is self-explanatory. |
| `tickets_url` | URL for ticket reservations.  If absent, "tickets by DM" is displayed instead. |
| `other_artists` | List of other artists on the lineup. Wrap with `<span lang="xx">` as appropriate. |

Document content is ignored.
