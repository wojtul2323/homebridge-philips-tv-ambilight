# Homebridge Philips TV Ambilight X

This plug-in provides support for Homebridge Philips TV Ambilight. It is a fork of [Konrad Knitter](https://github.com/konradknitter)'s [Homebridge Philips TV Ambilight](https://github.com/konradknitter/homebridge-philips-tv-ambilight) with a few enhancements, including:

- The configuration no longer has to be manually added/edited because `config.schema.json` is now correct.
- The Hue, Saturation and Brightness leves are now set correctly on the TV. The Homebridge scales have been translated from 360, 100, 100 to 255, 255, 255 before being sent-to/read-from the TV.

The decision to fork instead of submit a pull request was because the original project had a few issues and it had not been updated in over 2 years at the time or this fork, despite [a pull request](https://github.com/konradknitter/homebridge-philips-tv-ambilight/pull/6) from [TheVosh](https://github.com/TheVosh) being present for most of that time. Since pull requests were being ignored, I decided to create and publish this fork so that the fixes would be available directly from the homebridge UI.

## Info

Plug-in tested on:

- 55OLED856 ( API 6.1.0 )
- 49PUS7101 ( API 6.2.0 )
- 75PUS7354 ( API 6.4.0 )

Working:

- Turning on Ambilight. Including Wake over LAN.
- Control of Color.

What's next?

- Switch of Ambilight modes
- ... ?

This roadmap should led to 1.0 release.

# Authentication

Authentication is not needed for models I tested. Ambilight is supported on unauthorized port 1925.

# Plug-in configuration

The plugin can be easily configured from the web UI. To manually configure, add the following object to the accessories array in the config JSON

```
    {
        "accessory": "PhilipsTVAmbilightX",
        "name": "TV Ambilight",
        "ip": "IP ADDRESS",
        "macAddress": "MAC ADDRESS"
    }
```

# References

[Key knowledge about Philips TV APIs](https://github.com/eslavnov/pylips/wiki)
