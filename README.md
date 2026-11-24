# MARV's Mix Bench

A phone demo for technicians who mix paint on site from tinters. It does two jobs:

- **Scale a mix.** Enter the recipe as sent, the amount the job needs and the scale's precision. The app gives the weight of each tinter. Anything too light to weigh is converted to millilitres for a syringe, and if a tinter is too small even for that, the app gives the smallest batch that can be measured properly.
- **Fix a mix.** Pick what you are mixing and what is wrong with it (too green, too light and so on). MARV names the tinter to add, how strong it is, and a second option.

A third tab lists the eleven tinters with their codes, material numbers and densities.

## Status

This is a demo, not a finished tool. Three things are placeholders and are labelled as such on screen:

- **The example recipe is invented.** It is not a real formulation.
- **The Fix a mix advice is a draft.** It was written from the notes on the tin labels and standard colour practice. Technical has not signed it off.
- **The syringe sizes and the 0.10 ml cut-off are assumptions** until the stockroom confirms what technicians carry.

It is not a colour matcher. It does not identify a colour or produce a recipe, and it holds no licensed formulation data.

## Running it

Open `index.html` in a browser. There is no build step and no server. Everything is in that one file, plus three images in `images/`.

## How the scaling works

- A scale can be out by half its smallest step. To keep that error under about 5%, each tinter must weigh at least ten steps: 10 g on a 1 g scale, 1 g on a 0.1 g scale.
- Anything lighter is converted from grams to millilitres using the density printed on the tin.
- Below 0.10 ml a 1 ml syringe is not accurate enough either, so the app recommends a bigger batch.

## Where the data comes from

Tinter codes, material numbers, densities and mixing notes are from the labels on the tins, as recorded in the Colour Tool feasibility report of 13 October 2026. The strength ratings for the two Phthalos and the two oxides come from that report. The other strength ratings are a draft for Technical to confirm.
