# Yarukoto for Home Assistant

A Home Assistant custom integration that exposes lists from a self-hosted
[Yarukoto](https://yarukotoapp.com) server as Home Assistant to-do lists.

## Install with HACS

1. In HACS, open **Integrations**, then choose **Custom repositories**.
2. Add `https://github.com/wyne/yarukoto-home-assistant` as an **Integration**.
3. Install **Yarukoto** and restart Home Assistant.
4. In Home Assistant, open **Settings → Devices & services → Add integration**,
   search for **Yarukoto**, and enter your server URL. Home Assistant shows a
   sign-in code; approve it from **Settings → Add a device** in Yarukoto.

See the [Yarukoto Home Assistant guide](https://docs.yarukotoapp.com/integrations/home-assistant/)
for server and authentication details.

## Development

This repository owns only the Home Assistant integration. The Yarukoto apps,
server, and documentation live in [wyne/yarukoto](https://github.com/wyne/yarukoto).

```bash
python -m venv .venv
source .venv/bin/activate
pip install -r tests/requirements.txt
pytest -c tests/pytest.ini
```

Releases are created automatically when the version in
`custom_components/yarukoto/manifest.json` changes on `main`.

