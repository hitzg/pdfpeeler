# pdfpeeler
Remove margins from pdf files.

This is a small utility to process pdf files and remove white margins. 
It is very similar to (and inspired by) [PDFCrop](http://pdfcrop.sourceforge.net/), but adds the functionality to get a unified page size in the resulting pdf. 
This is especially useful when removing margins before printing.
Other than that, it is very basic and not extensively tested.

#### Installation

```bash
python setup.py install                # using `sudo` might be necessary
```  

#### Example

```bash
pdfpeeler.py somepdf.pdf
```

#### Usage
```
usage: pdfpeeler.py [-h] [-p] [-i] [-v] [-m MARGINS] [-o OUTFILE]
                    infile [infile ...]

Peel those large margins off your pdfs

positional arguments:
  infile                Input files to be processed

optional arguments:
  -h, --help            show this help message and exit
  -p, --page-wise       Process each page individually
  -i, --inches          Margins are specified in inches otherwise in mm
  -v, --verbose         Be verbose
  -m MARGINS, --margins MARGINS
                        Extra margins to add. Either this is a float, or a
                        comma separated list of 4 floats (left, bottom, right,
                        top)
  -o OUTFILE, --output-file OUTFILE
                        The output filename. This is only applicable if only
                        one input file is specified

```

