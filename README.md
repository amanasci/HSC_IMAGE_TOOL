# HSC IMAGE TOOL

This tool can bes used to get bulk rgb images from HSC. This is a fork of the official PD3 data access tool with added multi-threaded support.

Multi threading helps to speed up the image genration task, and is particularly useful when dealing with large amount of sources.

Original tool:
[PD3 Official Data Access Tool](https://hsc-gitlab.mtk.nao.ac.jp/ssp-software/data-access-tools/-/tree/master/pdr3/colorPostage)

## Basic Usage

```bash

cat > coords.txt <<EOT
# ra         dec             outfile(optional)
33.995270    -5.011639       a.png
33.994442    -4.996707       b.png
33.994669    -5.001553       c.png
33.996395    -5.008107       d.png
33.995679    -4.993945       e.png
33.997352    -5.010902       f.png
33.997315    -5.012523       g.png
33.997438    -5.011647       h.png
33.997379    -5.010878       i.png
33.996636    -5.008742       j.png
EOT

python colorPostage.py --user YOUR_ACCOUNT --outDir pngs coords.txt


```
