# KW Ride Compare

Compare estimated fares for Uber, Lyft, licensed taxis and GRT across Kitchener, Waterloo and Cambridge, Ontario.

Enter a pickup and drop-off, and the app ranks every option by price with a likely range, pickup wait and door-to-door time. Each result links to the Uber or Lyft app with the trip pre-filled, so you can confirm the real price before booking.

It's a single static page (`index.html`) with no build step and no API keys.

## Where the numbers come from

| Service | Source | Confidence |
|---|---|---|
| UberX, Comfort, XL | Fitted to live Uber quotes, 10 Oct 2026 | Good, but based on only two trips |
| Lyft, Lyft XL | Rate-card estimates | Low: probably overestimates longer trips |
| Licensed taxi | Region of Waterloo Taxi-Cab By-law 16-044 ($4.50 drop, $2.30/km, $35/h waiting) | High |
| GRT bus / ION | GRT single-ride fare ($4.00) | High |

**Surge** and **pickup times** are rule-of-thumb guesses based on time of day, day of week, weather and distance to busy areas. If Uber or Lyft shows a surge, enter it in the Surge box.

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
