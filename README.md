# Video delivery requirement templates

Plain-text templates for checking a video delivery **before** you send it: which files must exist, and the width, height and duration each one must have.

Each example has two files:

- `CHECKLIST.md` — a human-readable checklist you can copy into a ticket or email.
- `requirements.json` — the same terms in a small JSON format.

## Examples

- [`examples/fictional-launch-campaign`](examples/fictional-launch-campaign) — one 15-second spot delivered as 16:9, 9:16 and 1:1. Fictional client terms.
- [`examples/fictional-social-cutdowns`](examples/fictional-social-cutdowns) — four social versions of one campaign: 6-second 16:9 bumper, 15-second 9:16 and 1:1, 30-second 16:9. Fictional client terms.

## Client terms vs. platform recommendations

The examples describe what a (fictional) client asked for. They are **not** platform specifications. Platform guidance changes; check the source each time. As of 2026-10-29:

- YouTube lists 16:9 as the standard aspect ratio and recommends sizes such as 1920×1080 and 3840×2160 ([YouTube Help](https://support.google.com/youtube/answer/6375112)).
- TikTok in-feed ads (non-Spark): vertical 9:16 at 540×960 or larger, horizontal 16:9 at 960×540 or larger, square 1:1 at 640×640 or larger, up to 10 minutes ([TikTok Ads Help](https://ads.tiktok.com/help/article/video-ads-specifications)).

## JSON format

```json
{"version":1,"requirements":[{"name":"launch_16x9.mp4","width":1920,"height":1080,"duration":15,"tolerance":0.1}]}
```

`duration` and `tolerance` are in seconds.

## Checking files against the list

You can check by hand with the checklist. If you deliver many versions, [Video Delivery Checker](https://spinix0.gumroad.com/l/video-delivery-checker) is a small offline HTML tool (paid, made by the author of this repository) that compares the video files you select in your browser with a requirements list: missing, extra and duplicate files, width, height and duration. It does not check codec, frame rate, audio or content.

## License

Templates: CC0 — copy and adapt freely.
