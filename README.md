# XiHei Partner
晰黑伴侣：一款用来与「IPAexゴシック」「霞鹜新晰黑」「霞鹜晰黑」搭配的西文字体。A Latin font designed to be used alongside IPAexGothic, LXGW Neo XiHei and LXGW XiHei.

## Introduction / 字体简介

XiHei Partner is a Latin font derived from [Mona Sans](https://github.com/github/mona-sans). It was created by extracting static weights from the variable version of Mona Sans and freezing the OpenType style set, and can be used in conjunction with [IPAexGothic](https://moji.or.jp/ipafont), [LXGW Neo XiHei](https://github.com/lxgw/LxgwNeoXiHei), or [LXGW XiHei](https://github.com/lxgw/LxgwXiHei) in environments that support multi-font calling.

「晰黑伴侣」是基于 [Mona Sans](https://github.com/github/mona-sans) 衍生的西文字体，基于可变版 Mona Sans 提取静态字重并冻结 OpenType 样式集制成，可在支持多个字体调用的环境下将该字体与[「IPAexゴシック」](https://moji.or.jp/ipafon)[「霞鹜新晰黑」](https://github.com/lxgw/LxgwNeoXiHei)或[「霞鹜晰黑」](https://github.com/lxgw/LxgwNeoXiHei)搭配。

### How to make it / 制作方法

- Use [fonttools](https://github.com/fonttools/fonttools) to extract the 365 and 760 weights (corresponding to the Regular and Bold weights of Mona Sans 2.001 and earlier versions, respectively) as the Regular and Bold weights.
- 利用 [fonttools](https://github.com/fonttools/fonttools) 分别提取 365 和 760 字重（分别对应 Mona Sans 2.001 及以前版本的 Regular 和 Bold 字重），作为 Regular 和 Bold 字重。
- For the monospaced font XiHei Partner Mono, fonttools was used to determine a width of 87.08, establishing a 1:2 width ratio between Western characters and Chinese characters.
- 对于等宽字体 XiHei Partner Mono，利用 fonttools 提取 87.08 宽度，使西文与汉字宽度 1:2 对应。
- Use the [OpenType Feature Freezer](https://github.com/twardoch/fonttools-opentype-feature-freezer) to freeze the following OpenType features: `ss01`, `ss03`, `ss05`, `ss07`, `ss09`, `ss10`.
- 利用 [OpenType Feature Freezer](https://github.com/twardoch/fonttools-opentype-feature-freezer) 冻结以下 OpenType 特性： `ss01` `ss03` `ss05` `ss07` `ss09` `ss10`。
- Use FontCreator to merge outlines and edit font information.
- 利用 FontCreator 合并轮廓、修改字体信息。

## Get the fonts / 获取字体

- Go to the TTF folder in this repo to download the font.
- 进入本 repo 的 TTF 文件夹，获取字体。

## License / 授权方式

XiHei Partner is licensed under the [SIL Open Font License v1.1](https://openfontlicense.org/).

## Notes / 注意事项

- The characters included in this font are identical to those in Mona Sans, and there are currently no plans to follow upstream updates or expand the character set on our own.
- 本字体收录的字符与 Mona Sans 一致，且暂无跟进上游更新或自行扩充字符集的计划。
- Since SIL OFL 1.1 is incompatible with the IPA Font License 1.0, if you merge this font with a font licensed under the IPA license into a single font file using the [Warcraft Font Merger](https://github.com/nowar-fonts/Warcraft-Font-Merger) or similar methods, please keep it private and do not distribute it.
- 由于 SIL OFL 1.1 与 IPA Font License 1.0 不兼容，因此如果您通过[字体合并补全工具](https://github.com/nowar-fonts/Warcraft-Font-Merger)等方式将该字体与 IPA 协议字体合并到一个字体文件，请私下使用，切勿将其发布。

## Acknowledgement / 鸣谢

- [Mona Sans](https://github.com/github/mona-sans) by [GitHub Official](https://github.com/github) and [Degarism](https://degarism.com/)
- [foottools](https://github.com/fonttools/fonttools)
- [OpenType Feature Freezer](https://github.com/twardoch/fonttools-opentype-feature-freezer) by [Adam Twardoch](https://github.com/twardoch)
