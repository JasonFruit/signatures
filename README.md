# signatures

**Signatures** is a simple tool to make separate PDF files for each
bindable signature of a PDF book. It relies on pdfinfo and pdfbook,
the first of which is a standalone tool and the second of which is a
part of many LaTeX distributions.

It is especially good for converting a scanned PDF file of a public
domain book into a form more suitable for home binding.

## Usage ##

	usage: signatures [-h] [--start START] [--end END] [--pages PAGES]
					  [--size SIZE]
					  infile outdir

	A tool to generate bindable signatures from a PDF document

	positional arguments:
	  infile                the PDF file to process
	  outdir                the directory to which to write the output files

	optional arguments:
	  -h, --help            show this help message and exit
	  --start START, -s START
							the first page of the source document to process
							(default 1)
	  --end END, -e END     the final page of the source document to process
							(default last page)
	  --pages PAGES, -p PAGES
							the number of source-document pages per signature
							(default 16)
	  --size SIZE, -z SIZE  the size of the signature sheets, e.g. A4, letter
							(default letter)


Acceptable arguments for `--size/-z` are LaTeX paper sizes,
e.g. `a4paper`, `letter`, or sizes comprehensible to the `geometry`
package, e.g. {11in,17in}, {8in,14in}.
