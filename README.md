# Dots Energy CDN

Frontend assets for the Dots Energy P1 Dongle, served via [jsDelivr CDN](https://cdn.jsdelivr.net/gh/smartegrid/dots-cdn@main/).

The P1 Dongle firmware loads these files from the CDN at runtime. The dongle's `DSMRindexEDGE.html` (stored on LittleFS) references these assets.

## Files

| File | Description |
|------|-------------|
| `DSMRindex.min.js` | Main dashboard logic (settings, gauges, charts, history) |
| `DSMRindex_body.html` | Dashboard HTML structure (loaded dynamically) |
| `DSMRgraphics.min.js` | Chart rendering and graph utilities |
| `dal.min.js` | Data Access Layer — API calls to the dongle |
| `burnup.min.js` | Monthly burnup/cost chart logic |
| `DSMRindex_dots_dark.css` | Dark theme stylesheet |
| `chartjs-plugin-labels.min.js` | Chart.js label plugin |
| `dots_logo.webp` | Dots Energy logo |

## Directories

| Directory | Contents |
|-----------|----------|
| `lang/` | Translations (nl, en, de, se) |
| `assets/` | Images (EnergyID logo) |
| `favicon/` | Favicon and app icons |

## CDN Usage

The dongle's HTML references these files as:

```
https://cdn.jsdelivr.net/gh/smartegrid/dots-cdn@main/<filename>
```

jsDelivr caches files aggressively. After pushing changes, it can take a few minutes for the CDN to serve the new version. Force refresh on the dongle with `Ctrl+Shift+R`.

## Related Repositories

- [P1DongleFirmware](https://github.com/smartegrid/P1DongleFirmware) — ESP32 firmware
- [P1_METER_FRONTEND_DOTS](https://github.com/smartegrid/P1_METER_FRONTEND_DOTS) — Dashboard source, swagger, provisioning docs
