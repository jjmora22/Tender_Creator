Text Extractor and Formatter Script
This Python script extracts text from PDF and ODT documents, cleans and formats the text using natural language processing and regular expressions, and outputs a formatted Microsoft Word document.

Features
PDF Text Extraction:
Uses PyMuPDF to extract text blocks from PDFs, ignoring headers, footers, and digital seals.

ODT Text Extraction:
Uses odfpy to extract and preserve the text structure from ODT files.

Text Cleaning and Formatting:
Utilizes spaCy for sentence segmentation and regex to merge split lines, normalize bullet points, and format headings.

Word Document Generation:
Creates a formatted Word document (.docx) using python-docx.

Requirements
Python: 3.6 or higher
Dependencies:
PyMuPDF
Install with: pip install PyMuPDF
spaCy
Install with: pip install spacy
Then download the English model: python -m spacy download en_core_web_sm
odfpy
Install with: pip install odfpy
python-docx
Install with: pip install python-docx
Installation
Clone or Download:
Clone this repository or download the source code.

Install Dependencies:
Run the following commands in your terminal:

bash
Copiar
Editar
pip install PyMuPDF spacy odfpy python-docx
python -m spacy download en_core_web_sm
Usage
Prepare Input Files:
Place your input files (PPT.pdf, PCAP.pdf, ANEXOS.odt) in the same directory as the script. Alternatively, update the file paths in the script accordingly.

Run the Script:
Execute the script with:

bash
Copiar
Editar
python 1_extractor.py
Output:
The script will extract, clean, and format the text, then create a Word document named Pliego_Tecnico_Limpio_LocalNLP.docx in the same directory.

Customization
Input Files:
Modify the file paths in the script if your files are named differently or stored elsewhere.

Text Cleaning:
Adjust the regular expressions and spaCy processing within the script if you need customized text cleaning or formatting.

Output File:
Change the output file name by modifying the output_word variable in the script.

Contributing
Contributions, suggestions, and improvements are welcome. Feel free to fork this repository and submit a pull request.

License
MIT License with Attribution Requirement

Copyright (c) [2025] [Juan Jose de la Mora]

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

Any public use or distribution of the Software, or any derivatives thereof, must
include a clear attribution to the original source: “[Your Name or Organization]”.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY,
WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN
CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
