# MIDIC15 Web Config

MIDIC15 Web Config is an unofficial browser-based editor for configuring the 15 MIDI knobs on a [MIDIC15 device](https://null39.work/asset/midi%E8%AF%B4%E6%98%8E/Device/MIDIC15.html).

## Open The App

Open the published app here:

[https://over-keys.github.io/MIDIC15-Web-Config/](https://over-keys.github.io/MIDIC15-Web-Config/)

Use Chrome or Microsoft Edge, because the app uses Web MIDI.

## Local Use

You can also open `index.html` locally in a Web MIDI compatible browser.

If Web MIDI does not work from `file://`, serve the folder with a local web server or publish it over HTTPS.

## Basic Workflow

1. Connect the MIDIC15 device.
2. Open the app.
3. Click `MIDI` and allow MIDI access when the browser asks.
4. Confirm that the MIDI output and input are selected.
5. Edit each knob directly on the left panel:
   - `Channel`: MIDI channel, 1 to 16
   - `Mode`: `CC`, `ON`, or `OFF`
   - `Number`: CC or note number, 0 to 127
6. Use `Write` on a knob to send only that knob.
7. Use `Write All` to send all 15 knobs.

## Loading From The Device

Use `Load` on a knob to read one physical knob assignment.

Use `Load All` to read all 15 knobs in order. When prompted, move each physical knob slightly.

The latest received MIDI message is shown above the console.

## Import And Export

Use `Export` to save the current configuration as JSON.

Use `Import` to load a JSON configuration back into the app.

The current JSON format uses this order for each knob:

```json
{
  "channel": 1,
  "mode": "CC",
  "number": 20,
  "label": 1,
  "hardware": 2
}
```

`mode` can be `CC`, `ON`, or `OFF`.

## Notes

This is an unofficial tool and is not affiliated with the MIDIC15 manufacturer.

Close other MIDI apps, such as a DAW, if the browser cannot access the device.

If GitHub Pages does not show the latest version immediately, wait a moment or hard-refresh the page.
