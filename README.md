# images-upload-cli

> Upload images via APIs

[![PyPI version](https://img.shields.io/pypi/v/images-upload-cli)](https://pypi.org/project/images-upload-cli)
[![AUR version](https://img.shields.io/aur/version/python-images-upload-cli)](https://aur.archlinux.org/packages/python-images-upload-cli)
[![CI/CD](https://github.com/DeadNews/images-upload-cli/actions/workflows/python-app.yml/badge.svg)](https://github.com/DeadNews/images-upload-cli/actions/workflows/python-app.yml)
[![pre-commit.ci](https://results.pre-commit.ci/badge/github/DeadNews/images-upload-cli/main.svg)](https://results.pre-commit.ci/latest/github/DeadNews/images-upload-cli/main)
[![codecov](https://codecov.io/gh/DeadNews/images-upload-cli/branch/main/graph/badge.svg?token=OCZDZIYPMC)](https://codecov.io/gh/DeadNews/images-upload-cli)

## Installation

PyPI

```sh
pip install images-upload-cli
# or
pipx install images-upload-cli
```

AUR

```sh
yay -S python-images-upload-cli
```

## Hostings

| host                                           | key required | return example                                       |
| :--------------------------------------------- | :----------: | :--------------------------------------------------- |
| [catbox](https://catbox.moe/)                  |      -       | `https://files.catbox.moe/{id}`                      |
| [fastpic](https://fastpic.org/)                |      -       | `https://i120.fastpic.org/big/2022/0730/d9/{id}.png` |
| [filecoffee](https://file.coffee/)             |      -       | `https://file.coffee/u/{id}.png`                     |
| [freeimage](https://freeimage.host/)           |      -       | `https://iili.io/{id}.png`                           |
| [gyazo](https://gyazo.com/)                    |      +       | `https://i.gyazo.com/{id}.png`                       |
| [imageban](https://imageban.ru/)               |      +       | `https://i2.imageban.ru/out/2022/07/30/{id}.png`     |
| [imagebin](https://imagebin.ca/)               |      -       | `https://ibin.co/{id}.png`                           |
| [imgbb](https://imgbb.com/)                    |      +       | `https://i.ibb.co/{id}/image.png`                    |
| [imgchest](https://imgchest.com/)              |      +       | `https://cdn.imgchest.com/files/{id}.png`            |
| [imgur](https://imgur.com/)                    |      -       | `https://i.imgur.com/{id}.png`                       |
| [pictshare](https://pictshare.net/)            |      -       | `https://pictshare.net/{id}.png`                     |
| [pixeldrain](https://pixeldrain.com/)          |      -       | `https://pixeldrain.com/api/file/{id}`               |
| [pixhost](https://pixhost.to/)                 |      -       | `https://img75.pixhost.to/images/69/{id}_img.png`    |
| [ptpimg](https://ptpimg.me/)                   |      +       | `https://ptpimg.me/{id}.png`                         |
| [screenshotting](https://screenshotting.site/) |      -       | `https://screenshotting.site/i/{id}.png`             |
| [smms](https://sm.ms/)                         |      +       | `https://s2.loli.net/2022/07/30/{id}.png`            |
| [sxcu](https://sxcu.net/)                      |      -       | `https://sxcu.net/{id}.png`                          |
| [telegraph](https://telegra.ph/)               |      -       | `https://telegra.ph/file/{id}.png`                   |
| [thumbsnap](https://thumbsnap.com/)            |      +       | `https://thumbsnap.com/i/{id}.png`                   |
| [up2sha](https://up2sha.re/)                   |      +       | `https://up2sha.re/media/raw/{id}.png`               |
| [uplio](https://upl.io/)                       |      +       | `https://upl.io/i/{id}.png`                          |
| [uploadcare](https://uploadcare.com/)          |      +       | `https://ucarecdn.com/{id}/img.png`                  |
| [vgy](https://vgy.me/)                         |      +       | `https://i.vgy.me/{id}.png`                          |

## Usage

```sh
Usage: images-upload-cli [OPTIONS] IMAGES...

  Upload images via APIs.

Options:
  -h, --hosting [catbox|fastpic|filecoffee|freeimage|gyazo|imageban|imagebin|imgbb|imgchest|imgur|pictshare|pixeldrain|pixhost|ptpimg|screenshotting|smms|sxcu|telegraph|thumbsnap|up2sha|uplio|uploadcare|vgy]
                                  [default: imgur]
  -b, --bbcode                    Add bbcode tags.
  -t, --thumbnail                 Add caption thumbnail and bbcode tags.
  -c, --clipboard / -C, --no-clipboard
                                  Copy result to clipboard.  [default: c]
  --version                       Show the version and exit.
  --help                          Show this message and exit.
```

## Env variables

```ini
CAPTION_FONT= # The default font is system dependent.

FREEIMAGE_KEY=
GYAZO_TOKEN=
IMAGEBAN_TOKEN=
IMGBB_KEY=
IMGCHEST_KEY=
IMGUR_CLIENT_ID=
PTPIMG_KEY=
SMMS_KEY=
THUMBSNAP_KEY=
UP2SHA_KEY=
UPLIO_KEY=
UPLOADCARE_KEY=
VGY_KEY=
```

You can set these in environment variables, or in `.env` file:

- Unix: `~/.config/images-upload-cli/.env`
- MacOS: `~/Library/Application Support/images-upload-cli/.env`
- Windows: `C:\Users\<user>\AppData\Roaming\images-upload-cli\.env`
