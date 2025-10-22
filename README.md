# ShareVolume

## Summary

This project was automatically generated to fulfill the following brief: *Your assigned company: AvalonBay Communities (AVB), CIK 0000915912.

Fetch https://data.sec.gov/api/xbrl/companyconcept/CIK0000915912/dei/EntityCommonStockSharesOutstanding.json (set a descriptive User-Agent per SEC guidance).
Read `.entityName`. Filter `.units.shares[]` for entries whose `fy` > "2020" and
includes a numeric `val`.
Save `data.json` with this structure:
`{"entityName": "AvalonBay Communities", "max": {"val": ..., "fy": ...}, "min": {"val": ..., "fy": ...}}`
where `max` and `min` refer to the highest and lowest `.val`. Break ties however you like.

Render a visually appealing `index.html` where:
- `<title>` and `<h1>` must include the live `entityName`.
- The max/min figures are clearly marked with these IDs:
  `share-entity-name`,
  `share-max-value`, `share-max-fy`,
  `share-min-value`, `share-min-fy`.

If the page is opened as `index.html?CIK=0001018724` (or any other 10-digit CIK),
`fetch()` from the SEC endpoint for that CIK using any proxy, e.g. AIPipe,
replace every ID listed above and the title and H1 without reloading the page.

Also commit the attachment uid.txt as-is.*

## Setup & Usage

This is a static web page. Simply open the deployed GitHub Pages URL to view and use the application.

## Code Explanation

The application is contained within a single `index.html` file. All styling is provided via a `<style>` tag and all logic is contained within a `<script>` tag.

## License

This project is licensed under the MIT License.