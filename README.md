# nterm demo clips

Captioned clips for the [nterm](https://github.com/e82eric/nterm) README, kept
here so the main repository stays small. They are recorded with the scripts in
nterm's `docs/demo` folder; see `docs/demo/record.ps1` there.

| Clip | Shows |
| --- | --- |
| `tour.gif` | Panes, layouts, workspaces, and floating panes |
| `copy-mode.gif` | Vim copy mode |
| `quick-select.gif` | Quick select |
| `pickers.gif` | Pickers |

To turn a recorded MP4 into a GIF:

```sh
ffmpeg -y -i tour.mp4 -vf "fps=10,scale=1200:-1:flags=lanczos,split[a][b];[a]palettegen=max_colors=64:stats_mode=diff[p];[b][p]paletteuse=dither=none:diff_mode=rectangle" tour.gif
```
