## Install CLI

### Using Scoop (Windows)

```powershell
scoop bucket add supersimple https://github.com/gosupersimple/scoop-bucket
scoop install supersimple
```

## Update CLI

```powershell
scoop update supersimple
```

## How it works

`bucket/supersimple.json` is the Scoop manifest. On every CLI release, the
[supersimple-cli](https://github.com/gosupersimple/supersimple-cli) deployment workflow runs
`update_manifest.yaml` here, which opens a PR with the new version, download URL and SHA256.
Merge the PR to make the new version available to `scoop update`.

## Development

To test the manifest locally on Windows, run

```powershell
scoop install .\bucket\supersimple.json
```
