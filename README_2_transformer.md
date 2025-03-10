# Proposal Generator

## Overview
This script automates the generation of a proposal document based on the requirements extracted from a tender document (PDF). It processes the tender specifications, ensures all requirements are met, and formats the output into a structured proposal document in Microsoft Word (.docx) format.

## Features
- **Extracts structured titles from a PDF** to use as section headings.
- **Analyzes and generates content** using AI based on technical requirements.
- **Ensures compliance** with required certifications, SLAs, and infrastructure needs.
- **Incremental Writing** to handle large proposals efficiently.
- **Avoids redundant content** while ensuring all necessary details are covered.
- **Supports Spanish Language Generation** to match the tender's language.
- **Resumes from last progress** if interrupted.

## Requirements
### Dependencies
Ensure you have the following Python libraries installed:
```sh
pip install pymupdf docx langdetect requests
```

### Required Files
- **Tender PDF** (`PPT.PDF`): Contains the section headings.
- **Technical Specifications Document** (`Pliego_Tecnico_Limpio.docx`): Contains the details needed for the proposal.

## How to Use
1. **Set Up API Key**
   - Replace `your_api_key_here` in `ProposalGenerator` with a valid API key.

2. **Run the Script**
   ```sh
   python proposal_generator.py
   ```

3. **Output**
   - The proposal document will be saved as `Final_Proposal.docx`.
   - A temporary file (`temp_proposal.docx`) is used to save progress.

## Handling Large Documents
- The script writes content incrementally to avoid memory overload.
- If interrupted, it resumes from the last saved section.
- The final proposal is formatted and structured for readability.

## Troubleshooting
### Blank Document Issue
- Check the console logs for missing titles.
- Ensure the API response is valid (check status codes).
- Verify that the `Pliego_Tecnico_Limpio.docx` contains readable content.

### API Issues
- If the API fails multiple times, try increasing the timeout in `requests.post()`.
- Verify that your API key is active and has enough quota.

### Formatting Issues
- The script automatically removes redundant content.
- Sections are bolded and structured properly in Word.

## Future Improvements
- Multi-language support for tenders in different languages.
- Improved NLP to optimize sentence restructuring while maintaining completeness.
- Integration with a database to store proposal templates for reusability.

## License
This project is open-source and can be modified for specific business needs.
