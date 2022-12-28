Everything is in `exploration.ipynb`. Summary from there:

# `pypdfium2` Exploration
This notebook serves as an exploration of solving a few basic problems with PDFs using the `pypdfium2` library.

**`pypdfium2`**
>[pypdfium2](https://github.com/pypdfium2-team/pypdfium2) is an ABI-level Python 3 binding to [PDFium](https://pdfium.googlesource.com/pdfium/+/refs/heads/main), a powerful and liberal-licensed library for PDF creation, inspection, manipulation and rendering.
>
>The project is built using [ctypesgen](https://github.com/ctypesgen/ctypesgen) and external [PDFium binaries](https://github.com/bblanchon/pdfium-binaries/). Its custom setup infrastructure provides a seamless packaging and installation process. A wide range of platforms and Python versions is supported with wheel packages.
>
> pypdfium2 includes helper classes to simplify common use cases, while the raw PDFium/ctypes API remains accessible as well.

**Tasks in this notebook**
- Loading a PDF into a PdfDocument object
- Rendering the pages of a PDF to images
- Identifying bounding boxes of text elements within a PDF page and annotating the image of the page with these bounding boxes.
  - Also includes scaling up the image to a higher resolution and adapting the bbox coordiantes.
- Identifying non-text elements and annotating their bounding boxes on the page
- Finding out the font used for each character across the PDF, and aggregating the results for use with any stylistic analysis.
  - This uses the raw PDFium API for access to PDFium functions that don't have python helpers implemented.