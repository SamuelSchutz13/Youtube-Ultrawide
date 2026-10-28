# YouTube-Ultrawide

Custom **uBlock Origin** filters that make YouTube use the full width of ultrawide monitors.

By default, YouTube caps the content width and limits how many videos appear per row, leaving large empty areas on the sides of 21:9 and 32:9 screens. These filters remove those limits and force a fixed grid of **8 videos per row**.

## Features

- Removes shelves from the home page (Shorts, news, etc.)
- Removes the maximum width limit of the video grid
- Home page always shows **8 videos per row**
- Channel pages stretched to full width (header, tabs and video grid)
- Channel pages always show **8 videos per row**

## Requirements

- [uBlock Origin](https://github.com/gorhill/uBlock) installed in your browser
- A wide screen (ultrawide recommended)

## Installation

1. Click the **uBlock Origin** icon in your browser toolbar.
2. Open the **Dashboard** (gear icon).
3. Go to the **My filters** tab.
4. Paste the filters below.
5. Click **Apply changes**.
6. Reload YouTube.

## Filters

## Customization

To change the number of videos per row, edit the value of `--ytd-rich-grid-items-per-row` in the filters:

```adblock
--ytd-rich-grid-items-per-row: 6 !important;
```

Suggested values:

| Resolution  | Videos per row |
|-------------|----------------|
| 2560x1080   | 6              |
| 3440x1440   | 7 – 8          |
| 5120x1440   | 8 – 10         |

To keep the home page shelves (Shorts, news, etc.), just remove the first filter (`:remove()`).

## Notes

- YouTube changes its layout often, so some selectors may stop working after an update.
- Filters only affect `www.youtube.com`.

## Contributing

Issues and pull requests are welcome. If a filter breaks after a YouTube update, feel free to open an issue.
