# KW Ride Compare

Compare estimated fares for Uber, Lyft, licensed taxis and GRT across Kitchener, Waterloo and Cambridge, Ontario.

Enter a pickup and drop-off, and the app ranks every option by price with a likely range, pickup wait and door-to-door time. Each result links to the Uber or Lyft app with the trip pre-filled, so you can confirm the real price before booking.

It's a single static page (`index.html`) with no build step and no API keys.

## Where the numbers come from

| Service | Source | Confidence |
|---|---|---|
| UberX | About $7.50 + $1.07/km including HST, off-peak, Oct 2026 (±8%) | Good for trips up to ~10 km; untested on longer ones |
| Comfort, XL | Fixed multiples of UberX (1.45× and 1.83×), from live quotes on 10 Oct 2026 | Fair |
| Lyft, Lyft XL | Rate-card estimates | Low: probably overestimates longer trips |
| Licensed taxi | Region of Waterloo Taxi-Cab By-law 16-044 ($4.50 drop, $2.30/km, $35/h waiting) | High |
| GRT bus / ION | GRT single-ride fare ($4.00) | High |

**Surge** and **pickup times** are rule-of-thumb guesses based on time of day, day of week, weather and distance to busy areas. The weekday surge is +5% in the morning rush and +15% in the evening rush, and the typical pickup wait is about 3–6.5 minutes. Weekend-night and weather surges are still untested guesses. If Uber or Lyft shows a surge, enter it in the Surge box.

You can edit every rate in the page under **Edit fare rates**. Edits are saved in your browser only.

## Services used

- [Photon](https://photon.komoot.io) for address search
- [OSRM](https://project-osrm.org) for driving distance and time
- [Open-Meteo](https://open-meteo.com) for the weather forecast

All three are free and use OpenStreetMap data.

## Run it locally

Open `index.html` in a browser, or serve the folder with any static file server.

## Disclaimer

These are estimates. Surge pricing, tolls, tips and promotions aren't included. Always confirm the price in the app before you book. This project isn't affiliated with Uber, Lyft or GRT.
