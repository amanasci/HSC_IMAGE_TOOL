# HSC IMAGE TOOL

This tool retrieves bulk RGB images from HSC. It is a fork of the official PD3 data access tool, enhanced with multi-threaded support to drastically speed up image generation—especially when processing large datasets.

**Original Tool:**  
[PD3 Official Data Access Tool](https://hsc-gitlab.mtk.nao.ac.jp/ssp-software/data-access-tools/-/tree/master/pdr3/colorPostage)

## Features

- **Bulk Image Retrieval:** Download multiple images simultaneously.
- **Multi-threaded Processing:** Leverage parallel execution to accelerate image generation.
- **Customizable Output:** Specify output filenames directly in your input coordinates file.

## Requirements

- Python 3.x
- [Pillow](https://python-pillow.org/)
- [Astropy](https://www.astropy.org/)
- [tqdm](https://tqdm.github.io/)

## Installation

1. Clone this repository.
2. Create a virtual environment and activate it:
   ```bash
   python -m venv .venv
   source .venv/bin/activate
   ```
3. Install the dependencies:
   ```bash
   pip install -r requirements.txt
   ```

## Basic Usage

1. Prepare an input file (e.g., `coords.txt`) with the following format:
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
   ```
2. Run the tool:
   ```bash
   python get_image.py --user YOUR_ACCOUNT --outDir pngs coords.txt
   ```


## Acknowledgements

Thanks to the developers of the original PD3 data access tool for laying the groundwork for this project.
