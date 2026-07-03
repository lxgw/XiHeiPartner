# XiHei Partner / 晰黑伴侣

A Latin font designed to be used alongside IPAexGothic, LXGW Neo XiHei and LXGW XiHei.

一款用来与「IPAexゴシック」「霞鹜新晰黑」「霞鹜晰黑」搭配的西文字体。

## Introduction / 字体简介

XiHei Partner is a Latin font derived from [Mona Sans](https://github.com/github/mona-sans). It was created by extracting static weights from the variable version of Mona Sans and freezing the OpenType stylistic sets. It is intended to be used in conjunction with [IPAexGothic](https://moji.or.jp/ipafont), [LXGW Neo XiHei](https://github.com/lxgw/LxgwNeoXiHei), or [LXGW XiHei](https://github.com/lxgw/LxgwXiHei) in environments that support **multi-font fallback**.

「晰黑伴侣」是基于 [Mona Sans](https://github.com/github/mona-sans) 衍生的西文字体。本字体从 Mona Sans 可变版本中提取静态字重，并冻结了 OpenType 样式集，适用于支持**多字体调用**的环境，可与[「IPAexゴシック」](https://moji.or.jp/ipafont)[「霞鹜新晰黑」](https://github.com/lxgw/LxgwNeoXiHei)或「[霞鹜晰黑](https://github.com/lxgw/LxgwXiHei)」搭配使用。

### How to make it / 制作方法

- Use the [OpenType Feature Freezer](https://github.com/twardoch/fonttools-opentype-feature-freezer) to freeze the following OpenType features: `ss01`, `ss03`, `ss05`, `ss07`, `ss09`, `ss10`. For the monospaced version, only `ss01`, `ss05` and `ss07` are frozen.
- 利用 [OpenType Feature Freezer](https://github.com/twardoch/fonttools-opentype-feature-freezer) 冻结以下 OpenType 特性：`ss01`、`ss03`、`ss05`、`ss07`、`ss09`、`ss10`。对于等宽版本，仅冻结 `ss01`、`ss05`、`ss07`。
```
pyftfeatfreeze -n -v -f ss01,ss03,ss05,ss07,ss09,ss10 -S -U "Mod" MonaSansVF[wdth,opsz,wght].ttf MonaSansVFMod[wdth,opsz,wght].ttf
pyftfeatfreeze -n -v -f ss01,ss03,ss05,ss07,ss09,ss10 -S -U "Mod" MonaSansVF-Italic[wdth,opsz,wght].ttf MonaSansVFMod-Italic[wdth,opsz,wght].ttf
pyftfeatfreeze -n -v -f ss01,ss05,ss07 -S -U "Mod" MonaSansMonoVF[wdth,wght].ttf MonaSansMonoVFMod[wdth,wght].ttf
```
- Use [fonttools](https://github.com/fonttools/fonttools) to extract weights 365 and 737 (corresponding to the Regular and Bold weights of [Mona Sans v2.000](https://github.com/github/mona-sans/releases#release-v2.0) and earlier versions, respectively) as the Regular and Bold weights.
- 利用 [fonttools](https://github.com/fonttools/fonttools) 分别提取 365 和 737 字重（对应 [Mona Sans v2.000](https://github.com/github/mona-sans/releases#release-v2.0) 及以前版本的 Regular 和 Bold 字重），作为本字体的 Regular 和 Bold 字重。
```
fonttools varLib.mutator MonaSansVFMod[wdth,opsz,wght].ttf wdth=100 wght=365 opsz=20 -o XiHeiPartner-Regular.ttf
fonttools varLib.mutator MonaSansVFMod-Italic[wdth,opsz,wght].ttf wdth=100 wght=365 opsz=20 -o XiHeiPartner-Italic.ttf
fonttools varLib.mutator MonaSansVFMod[wdth,opsz,wght].ttf wdth=100 wght=737 opsz=20 -o XiHeiPartner-Bold.ttf
fonttools varLib.mutator MonaSansVFMod-Italic[wdth,opsz,wght].ttf wdth=100 wght=737 opsz=20 -o XiHeiPartner-BoldItalic.ttf
```
- For the monospaced version XiHei Partner Mono, fonttools was used to set the width to 87.08, establishing a 1:2 width ratio between Latin characters and CJK characters.
- 对于等宽版本 XiHei Partner Mono，利用 fonttools 将宽度设定为 87.08，使西文字符与 CJK 字符的宽度比为 1:2。
```
fonttools varLib.mutator MonaSansMonoVFMod[wdth,wght].ttf wdth=87.08 wght=365 -o XiHeiPartnerMono-Regular.ttf
fonttools varLib.mutator MonaSansMonoVFMod[wdth,wght].ttf wdth=87.08 wght=737 -o XiHeiPartnerMono-Bold.ttf
```
- Use FontCreator to edit font information.
- 利用 FontCreator 修改字体信息。

## Get the fonts / 获取字体

- Go to the `TTF` folder in this repository to download the font files.
- 进入本仓库的 `TTF` 文件夹获取字体文件。
- The `FCP` folder contains FontCreator project files, which require FontCreator v15.0.0.3048 or later to open.
- `FCP` 文件夹内提供 FontCreator 工程文件，需要 v15.0.0.3048 或以上版本的 FontCreator。

## License / 授权方式

XiHei Partner is licensed under the [SIL Open Font License v1.1](https://openfontlicense.org/).

「晰黑伴侣」依据 [SIL Open Font License v1.1](https://openfontlicense.org/) 开源协议发布。

## Notes / 注意事项

- The characters included in this font are identical to those in [Mona Sans v2.027](https://github.com/github/mona-sans/releases/tag/v2.0.27). There are currently no plans to follow upstream updates or expand the character set independently.
- 本字体收录的字符与 [Mona Sans v2.027](https://github.com/github/mona-sans/releases/tag/v2.0.27) 一致，暂无计划跟进上游更新或自行扩充字符集。
- Since SIL OFL 1.1 is **incompatible** with the IPA Font License 1.0, if you merge this font with a font licensed under the IPA license into a single font file using the [Warcraft Font Merger](https://github.com/nowar-fonts/Warcraft-Font-Merger) or similar tools, please keep the merged file for private use only and **do not distribute it**.
- 由于 SIL OFL 1.1 与 IPA Font License 1.0 **不兼容**，如果您通过[字体合并补全工具](https://github.com/nowar-fonts/Warcraft-Font-Merger)等方式将该字体与 IPA 协议字体合并为单一字体文件，请仅限私下使用，**切勿对外发布**。

## Acknowledgement / 鸣谢

- [Mona Sans](https://github.com/github/mona-sans) by [GitHub Official](https://github.com/github) and [Degarism](https://degarism.com/)
- [fonttools](https://github.com/fonttools/fonttools)
- [OpenType Feature Freezer](https://github.com/twardoch/fonttools-opentype-feature-freezer) by [Adam Twardoch](https://github.com/twardoch)
