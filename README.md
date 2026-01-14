# 🔍 AI-Driven PDF Comparator

[![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)](https://www.python.org/downloads/)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![Status](https://img.shields.io/badge/Status-Active-success.svg)]()

> **Intelligent document comparison tool that automates the analysis of PDF files with advanced text, table, and image detection capabilities.**

AI-Driven PDF Comparator performs comprehensive comparisons across multiple dimensions including text content, metadata fields, tabular data, and embedded images using perceptual hashing algorithms. It generates professional, visually appealing HTML reports that highlight all differences in an easy-to-understand format.

---

## ✨ Features

### 🎯 Core Capabilities

- **📄 Text Comparison** - Line-by-line text difference detection with unified diff output
- **🏷️ Metadata Extraction** - Automatic extraction and comparison of document metadata (Date, Brand, Product, Description, Barcode, etc.)
- **📊 Table Analysis** - Advanced table extraction and cell-by-cell comparison with structure validation
- **🖼️ Image Detection** - Perceptual image hashing to detect visual differences with similarity percentages
- **📑 HTML Reports** - Beautiful, responsive HTML reports with color-coded differences and visual analytics

### 🔬 Advanced Features

- **Multiple Hash Algorithms** - Average Hash, Perceptual Hash (pHash), and Difference Hash (dHash)
- **Similarity Scoring** - Percentage-based similarity metrics for quantitative analysis
- **Smart Table Extraction** - Handles complex table structures with metadata and measurements
- **Comprehensive Logging** - Detailed console output for tracking comparison progress
- **Error Handling** - Robust exception handling with detailed error messages

---

## 🚀 Quick Start

### Prerequisites

- Python 3.8 or higher
- pip package manager

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/ai-pdf-comparator.git
   cd ai-pdf-comparator
   ```

2. **Install required dependencies**
   ```bash
   pip install PyMuPDF pdfplumber Pillow pandas imagehash
   ```

### Usage

#### Python Script

```python
from pdf_compare_solution import PDFComparator

# Initialize the comparator
comparator = PDFComparator('document1.pdf', 'document2.pdf')

# Run the comparison
results = comparator.run_comparison()

# Print summary to console
comparator.print_summary()

# Generate HTML report
comparator.generate_html_report()
```

#### Jupyter Notebook (Google Colab)

1. Open `pdf_compare_solution.ipynb` in Google Colab
2. Run cells sequentially (1-16)
3. Upload your PDF files when prompted
4. Download the generated HTML report

---

## 📊 Example Output

### Console Summary
```
======================================================================
COMPARISON SUMMARY
======================================================================
Files: P001 2.pdf vs P002 2.pdf
----------------------------------------------------------------------
Metadata: 6 differences
Text: 1 pages
Tables: 2 tables
  -> 28 cells changed
Images: 1 differences
  -> Image 1: 43.8% similar, 56.2% different
======================================================================
```

### HTML Report Features

- **Executive Summary** - Quick overview of all detected differences
- **Text Differences** - Side-by-side diff view with syntax highlighting
- **Table Comparisons** - Color-coded tables showing cell-level changes
- **Image Analysis** - Visual similarity bars with detection algorithm details
- **Business Impact** - Automated insights and conclusions

---

## 🛠️ Technologies Used

| Technology | Purpose |
|-----------|---------|
| **PyMuPDF (fitz)** | PDF text and image extraction |
| **pdfplumber** | Advanced table detection and extraction |
| **Pillow (PIL)** | Image processing and manipulation |
| **imagehash** | Perceptual image comparison algorithms |
| **pandas** | Data structure management for tables |
| **difflib** | Text difference generation |

---

## 📁 Project Structure

```
ai-pdf-comparator/
│
├── pdf_compare_solution.py      # Main Python script
├── pdf_compare_solution.ipynb   # Jupyter Notebook version
├── pdf_compare_solution.html    # Sample generated report
├── README.md                     # Project documentation
└── requirements.txt              # Python dependencies
```

---

## 🔧 How It Works

### 1️⃣ **Extraction Phase**
- Extracts text from all pages using PyMuPDF
- Parses metadata using regex patterns
- Detects and extracts tables using pdfplumber
- Identifies and extracts images (≥200x200 pixels)

### 2️⃣ **Comparison Phase**
- **Text**: Uses `difflib.unified_diff` for line-by-line comparison
- **Metadata**: Field-by-field comparison with structured output
- **Tables**: Cell-by-cell comparison with type-specific handling
- **Images**: Three perceptual hash algorithms (Average, Perceptual, Difference)

### 3️⃣ **Reporting Phase**
- Generates comprehensive HTML report with CSS styling
- Color-codes differences (red for PDF1, green for PDF2)
- Calculates similarity percentages for visual elements
- Provides business impact analysis and recommendations

---

## 💡 Use Cases

✅ **Quality Assurance** - Automated validation of updated product specifications  
✅ **Version Control** - Track changes across document revisions  
✅ **Compliance Verification** - Ensure regulatory document consistency  
✅ **Product Management** - Compare product specification sheets  
✅ **Legal Documentation** - Detect changes in contracts and agreements  
✅ **Technical Documentation** - Monitor updates to technical manuals  

---

## 📸 Screenshots

### HTML Report Preview
The generated report includes:
- 🎨 Gradient backgrounds and modern UI design
- 📊 Interactive comparison tables
- 📈 Visual similarity progress bars
- 🎯 Executive summary with key metrics
- 💼 Business impact analysis

---

## 🤝 Contributing

Contributions are welcome! Here's how you can help:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

---

## 📋 Requirements

```txt
PyMuPDF>=1.23.0
pdfplumber>=0.10.0
Pillow>=10.0.0
pandas>=2.0.0
imagehash>=4.3.0
```

---

## 🎯 Roadmap

- [ ] Add support for multi-page comparisons
- [ ] Implement PDF merging and splitting
- [ ] Add command-line interface (CLI)
- [ ] Support for batch processing
- [ ] Export to JSON/CSV formats
- [ ] Add web-based UI
- [ ] Docker containerization
- [ ] API endpoint creation

---

## ⚙️ Configuration

The tool can be customized by modifying:

- **Image size threshold**: Minimum 200x200 pixels (configurable)
- **Hash similarity threshold**: Default >3 for differences (adjustable)
- **Table extraction strategy**: Lines-based with 5px tolerance
- **Output file naming**: Default `pdf_compare_solution.html`

---

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## 👤 Author

**Your Name**

- GitHub: [@yourusername](https://github.com/yourusername)
- LinkedIn: [Your LinkedIn](https://linkedin.com/in/yourprofile)

---

## 🙏 Acknowledgments

- PyMuPDF team for excellent PDF processing capabilities
- pdfplumber for robust table extraction
- imagehash library for perceptual hashing algorithms

---

## 📞 Support

If you encounter any issues or have questions:

1. Check the [Issues](https://github.com/yourusername/ai-pdf-comparator/issues) page
2. Create a new issue with detailed description
3. Contact via email: your.email@example.com

---

## ⭐ Show Your Support

If this project helped you, please give it a ⭐️!

---

<div align="center">
  
**Made with ❤️ for automated document analysis**

</div>
