# fluxcut-checksums

SHA-256 checksums of the files [Fluxcut](https://www.aigcflow.xyz) serves to AI agents: the
playbooks under `https://www.aigcflow.xyz/agents/v<N>/` and the `fluxcut-capture` wheels under
`https://www.aigcflow.xyz/agents/`.

This list lives here, apart from the site, on purpose: if a file on the site were changed, it would
no longer match this list. Published entries are never changed; a new release adds lines.

Check a download (Linux: `sha256sum -c`):

```bash
WHEEL=fluxcut_capture-0.2.0-py3-none-any.whl
curl -fsSLO https://www.aigcflow.xyz/agents/$WHEEL
curl -fsSL https://raw.githubusercontent.com/Flux-AI-Agent/fluxcut-checksums/main/SHA256SUMS \
  | grep " $WHEEL$" | shasum -a 256 -c
```

Setup for agents: https://www.aigcflow.xyz/connect
