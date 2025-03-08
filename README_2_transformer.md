# Proposal Generator

This Python script automates the process of generating proposal documents by analyzing technical requirements and transforming them into structured proposal text using AI. It currently generates multiple versions of the proposal but is in the process of being improved to consolidate all iterations into a single document.

## Features

- **Extracts Proposal Components**  
  Parses an existing proposal document (`Resumen_Propuesta.docx`) to identify key sections.

- **Processes Technical Specifications**  
  Reads a technical document (`Pliego_Tecnico_Limpio.docx`) and extracts individual requirements.

- **AI-Based Text Generation**  
  Uses the Deepseek API to convert technical requirements into refined proposal language.

- **Structured Output**  
  Generates a `propuesta_vers1b.docx` document with AI-enhanced content.

- **Automated Logging & Error Handling**  
  Provides progress updates and retries failed API requests with exponential backoff.

## Installation

### **1. Clone the Repository**
git clone https://github.com/yourusername/proposal-generator.git
cd proposal-generator

### **2. Install Dependencies**
Ensure you have **Python 3.6+** installed, then install the required packages:
pip install -r requirements.txt


### **3. Set Up the API Key**
Before running the script, you need to **set your API key as an environment variable**:
- **Linux/macOS**:
  export DEEPSEEK_API_KEY="your-api-key-here"
- **Windows (PowerShell)**:
  $env:DEEPSEEK_API_KEY="your-api-key-here"


## Usage

### **1. Prepare Input Files**
Ensure the following files exist in the same directory as the script:
- `Pliego_Tecnico_Limpio.docx` (Technical Specification Document)
- `Resumen_Propuesta.docx` (Proposal Summary Document)

### **2. Run the Script**
Execute the script:
python 2_transformer.py


### **3. Output**
- The script will create `propuesta_vers1b.docx` containing AI-generated proposal text.
- Currently, multiple versions of the proposal are included in the output, but improvements are being made to consolidate them into a **single structured document**.

## Known Issues & Work in Progress
- **Multiple proposal iterations instead of a single consolidated version**  
  - This is actively being improved to ensure that all AI-generated content is properly structured within a unified document.

- **Formatting improvements**  
  - Additional refinements are planned to improve section organization and ensure consistency.

## Contributing

Contributions and suggestions are welcome! Feel free to fork the repository, submit pull requests, or report issues.

## License

License MIT License with Attribution Requirement

Copyright (c) [2025] Juan Jose de la Mora

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

Any public use or distribution of the Software, or any derivatives thereof, must include a clear attribution to the original source: “[Your Name or Organization]”.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

