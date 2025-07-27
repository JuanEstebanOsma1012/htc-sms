# Example Folder File Summary

This document provides a comprehensive overview of each file in the example folder, explaining their purpose, functionality, and role in creating the Journal of Metaverse LaTeX template.

## 1. Jmv.tex - Main LaTeX Document Template

### Purpose
The `Jmv.tex` file is the main LaTeX document template for academic papers formatted according to the "Journal of Metaverse" style. This is a complete, ready-to-use template that demonstrates proper academic paper formatting.

### Key Features

#### Document Setup
- **Document Class**: Uses `article` class with A4 paper size
- **Page Margins**: Set to 1.5cm left/right, 2.54cm top/bottom using the geometry package
- **Package Dependencies**: Includes essential packages for academic writing:
  - `graphicx`: Image handling
  - `hyperref`: Hyperlinks and PDF metadata
  - `amsmath`, `amssymb`: Mathematical symbols and equations
  - `titlesec`: Custom section formatting
  - `fancyhdr`: Custom headers and footers
  - `multicol`: Multi-column layout support
  - `cite`: Citation management

#### Formatting Specifications
- **Section Numbering**: 
  - Sections use Roman numerals (I., II., III.)
  - Subsections use italic capital letters (A., B., C.)
  - Subsubsections use italic Arabic numerals (1., 2., 3.)
- **Title Formatting**: Sections are centered, large, and in small caps
- **Spacing**: Single spacing with 6pt paragraph spacing
- **Tables and Figures**: Numbered using Roman numerals

#### Header and Footer Configuration
- **First Page**: Special header with journal information, submission dates, and DOI
- **Subsequent Pages**: Simple "Journal of Metaverse" header
- **Footer**: Contains Creative Commons licensing information and page numbers

#### Content Structure
The template includes:
- Title with APA citation format in footnote
- Multi-column author block with ORCID integration
- Abstract with keywords
- Complete paper sections (Introduction, Methods, Results, Discussion, Conclusion)
- Bibliography with 8 sample references
- Academic integrity statements (funding, conflicts, data availability, etc.)

### Usage
This file serves as a template for researchers submitting to the Journal of Metaverse. Authors can replace the placeholder content with their actual research while maintaining the required formatting.

## 2. Jmv.pdf - Compiled Output

### Purpose
The `Jmv.pdf` file is the compiled PDF version of the `Jmv.tex` LaTeX document. It demonstrates the final appearance of papers formatted according to the Journal of Metaverse style guidelines.

### Contents
- Shows the exact visual output of the LaTeX template
- Demonstrates proper formatting, spacing, and layout
- Serves as a reference for authors to see how their final paper should appear
- Includes all visual elements: headers, footers, images, tables, and bibliography

### Usage
This PDF serves as:
- A visual reference for the journal's formatting requirements
- A sample for authors to compare their work against
- Documentation of the template's output for quality assurance

## 3. cite.sty - Citation Style Package

### Purpose
The `cite.sty` file is a LaTeX style package that provides enhanced citation formatting capabilities, specifically designed to create compressed, sorted lists of numerical citations.

### Key Features

#### Citation Compression
- Converts sequential citations like `[11,12,13,14,15,16]` into compressed format `[11-16]`
- Automatically sorts citation numbers in ascending order
- Handles mixed citation lists efficiently

#### Technical Implementation
- **Version**: 3.0 (October 1992)
- **Author**: Donald Arseneau
- **License**: Free for non-commercial use
- **Compatibility**: Works with standard LaTeX citation systems

#### Core Functions
- `\citen`: Provides citation numbers without additional formatting
- `\@make@cite@list`: Creates sorted lists of citation numbers
- `\@compress@cite`: Compresses consecutive citation ranges
- Error handling for undefined citations

#### Usage in Document
- Automatically processes `\cite{}` commands
- Writes citation information to auxiliary files
- Integrates seamlessly with bibliography systems
- Provides warning messages for undefined citations

### Benefits
- Reduces visual clutter in documents with many citations
- Improves readability of citation-heavy sections
- Maintains consistency in citation formatting
- Saves space in printed documents

## 4. parskip.sty - Paragraph Spacing Package

### Purpose
The `parskip.sty` package modifies LaTeX's default paragraph formatting to use spacing between paragraphs instead of paragraph indentation, creating a more modern document appearance.

### Key Modifications

#### Paragraph Formatting
- **Paragraph Indentation**: Set to zero (`\parindent=\z@`)
- **Paragraph Spacing**: Set to 0.5 baseline skip with stretchable glue
- **Flexibility**: Includes `0pt plus 2pt` stretch for better page breaking

#### List Environment Adjustments
The package modifies list spacing to maintain consistency:
- `\parsep = \parskip`: Uses same spacing as paragraphs
- `\itemsep = \z@`: No additional spacing between items
- `\topsep = \z@`: No additional spacing before first item
- `\partopsep = \z@`: No extra spacing even after blank lines

#### Technical Details
- **LaTeX Format**: Requires LaTeX2e
- **Version**: 2001/04/09
- **Authors**: H. Partl (TU Wien), modified by Robin Fairbairns
- **Option**: `parfill` option available for paragraph fill adjustment

#### List Level Support
Provides consistent formatting for:
- First-level lists (`\@listI`)
- Second-level lists (`\@listii`)
- Third-level lists (`\@listiii`)

### Benefits
- Creates cleaner, more modern document appearance
- Improves readability by clearly separating paragraphs
- Maintains consistent spacing throughout the document
- Better suited for academic papers with complex content structure

### Usage in Journal Template
In the Jmv.tex template, this package works alongside manual spacing settings to create the journal's specific paragraph formatting requirements.

## File Relationships and Dependencies

### Integration Overview
All files work together to create a cohesive academic paper template:

1. **Jmv.tex** serves as the main document that imports and utilizes the other components
2. **cite.sty** handles citation formatting throughout the document
3. **parskip.sty** manages paragraph spacing and list formatting
4. **Jmv.pdf** demonstrates the final output of the combined system

### Dependencies
- The LaTeX document requires both .sty files to compile correctly
- Image files (cc-by.png, orcid.png, image.jpg) are referenced by the main document
- The citation system depends on proper bibliography formatting
- The paragraph spacing works in conjunction with other spacing commands in the main document

### Best Practices
- Keep all files in the same directory for proper compilation
- Ensure image files are present when compiling the document
- Use the template as a starting point while maintaining the formatting requirements
- Update placeholder content while preserving the structural elements

## Technical Requirements

### LaTeX Distribution
- Requires a modern LaTeX distribution (TeX Live, MiKTeX, etc.)
- Compatible with pdfLaTeX, XeLaTeX, and LuaLaTeX engines
- Requires standard LaTeX packages (most distributions include these by default)

### Compilation Process
1. Run LaTeX engine on Jmv.tex
2. Process bibliography if citations are updated
3. Run LaTeX again to resolve cross-references
4. Final compilation for proper page numbering and references

This example folder provides a complete, professional academic paper template suitable for submission to the Journal of Metaverse or adaptation for other academic publications.
