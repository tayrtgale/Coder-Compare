# Coder-Compare
Tool for establishing inter-coder reliability in ELAN in a timely and efficient manner - Support tool for research purposes - Not affiliated with ELAN 

Finds where coders disagree in their ELAN files.

Coder Compare reads each coder's `.eaf` files for the same recordings and lists every utterance where they differ, by recording and time stamp. It replaces the manual routine of exporting from ELAN, sorting in Excel, and comparing rows by eye.

Created by Taylor G. Morales Long.

## What it finds

| Finding | Meaning |
|---|---|
| Disagreement | The coders annotated the same utterance but gave it different codes |
| Different timing | Same tier, but the start or end time differs |
| Different tier | Same times, but the coders used different tiers |
| Missing | One coder has an annotation the other does not |

It also lists the pairs of codes that are most often confused.

## How to use it

1. Download `index.html` and open it in a browser. Nothing needs to be installed.
2. Name each file so it starts with the recording ID and ends with the coder, separated by underscores, for example `F004_task_TM.eaf`.
3. Choose the folder that holds all the `.eaf` files you want to compare.
4. Type the names of the tiers to compare, exactly as they appear in ELAN.
5. Click a recording to see its findings.

The page opens with made-up example data so you can see how it works first.

## Privacy

- Files are read inside the browser tab. They are never uploaded.
- The page makes no connection to any other site, and it works with no internet connection.
- Only `.eaf` files are read, and only the tiers you name. Video and audio are never opened.
- Nothing is stored. Closing the tab clears everything.

You can confirm this by turning off Wi-Fi after the page loads, or by watching the Network tab in your browser's developer tools.

## Checking the results

Click **Save Excel check file** to get a workbook that holds every annotation and every utterance, with the counts written as Excel formulas. Its Summary sheet recounts agreement straight from the raw annotations and compares that with the tool's own count.

## What it does not do

- **It does not calculate reliability.** Use ELAN's own inter-annotator reliability function for the figures you report. Coder Compare is for finding and resolving disagreements faster.
- **It needs identical times.** Two annotations count as the same utterance only when the tier, start time and end time are identical. It suits projects where every coder starts from the same pre-segmented file.
- **Tier names must match.** The same tier must have the same name in every coder's file.

## Testing so far

- The matching logic was checked against one real data set of 7 recordings and 2 coders, and against Excel formulas.
- The author has run it on real `.eaf` files from a coding project, as well as on small made-up test files.
- The code has not yet had an independent review.

Try it on one recording you have already checked by hand before relying on it.

## How it was made

The author designed the tool, decided how it should work, and tested it. The code was written with an AI assistant (Claude, by Anthropic) from the author's instructions.

## How to cite

Morales Long, T. G. (2026). *Coder Compare: finds coder disagreements in ELAN files* (Version 1.4) [Computer software].

## License

Released under the MIT License. See `LICENSE`.

The embedded fonts, IBM Plex Sans and IBM Plex Mono, are by IBM and are used under the SIL Open Font License 1.1. See `LICENSE-IBM-Plex-OFL.txt`.

Coder Compare is an independent tool. It is not affiliated with ELAN or with The Language Archive at the Max Planck Institute for Psycholinguistics.
