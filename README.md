# ⚠️ IMPORTANT WARNING ⚠️

**Using Sci-Hub can be a violation of copyright laws and is considered illegal in several countries. By using this repository and its associated tools, you acknowledge and accept all responsibilities and potential legal consequences. It is crucial to be informed about the legal regulations in your country or jurisdiction before using this software. The creators and contributors of this repository do not endorse or encourage illegal activities and are not responsible for any misuse or potential violations of law. Always prioritize and respect copyright laws and regulations.**

---
### Personal Note from the Creator:

I firmly believe that science should be free and it's vital for it to remain accessible to all. This belief drives my decision to share this repository, despite the potential legal implications. In a world striving for knowledge and progress, it's essential for scientific information to be openly available.

# Paper Scraper

Paper Scraper is a script designed to scrape academic papers from Sci-Hub using Selenium and the Chrome WebDriver. It automates the download process by taking a list of DOIs (Digital Object Identifiers) and saving the corresponding PDFs to the specified output folder. This tool is essential for researchers and academicians who need to download multiple papers from Sci-Hub in an automated and organized manner.

## Features
- Automatically downloads papers using a list of DOIs.
- Supports `.txt` and `.csv` formats for the DOI list.
- Customizable output folder.
- Debugging, caching, safe mode, and verbose options for advanced users.
- Easy integration with batch scripts for streamlined execution.

## Installation

1. **Clone the Repository:**
    ```
    git clone https://github.com/[your-github-username]/paper-scraper.git
    cd paper-scraper
    ```

2. **Set Up a Virtual Environment (Optional, but recommended):**
    ```
    python -m venv venv
    ```

3. **Activate the Virtual Environment:**
    - **Windows:**
        ```
        .\venv\Scripts\activate
        ```
    - **Linux/Mac:**
        ```
        source venv/bin/activate
        ```

4. **Install Required Packages:**
    ```
    pip install -r requirements.txt
    ```

## Usage

### Command Line

1. **Basic Usage:**
    ```
    python scrape_papers.py [path-to-doi-list] --output-folder [path-to-output-folder]
    ```

2. **Advanced Options:**
    ```
    python scrape_papers.py [path-to-doi-list] --output-folder [path-to-output-folder] --debug --no-cache --safe-mode --verbose [verbosity-level]
    ```

### Batch Script

Execute the provided batch script `scrape_papers.bat` by double-clicking on it or running it from the command line. This script is set up to use specific paths and verbosity options by default. Modify the script as needed.

## Options

- `doi_list_path`: Path to the file containing the list of DOIs. This file should be a `.txt` or `.csv` file with DOIs delimited by newlines or commas.

- `--output-folder`: Specifies the output directory where the downloaded papers will be saved.

- `--debug`: Enables debug mode for detailed logs.

- `--no-cache`: Disables caching. By default, a list of papers not found on Sci-Hub is saved to a cache file.

- `--safe-mode`: Increases maximum tries for each paper and validates each download. If a paper is not downloaded correctly, the script will attempt to download it again.

- `--verbose`: Sets the verbosity level. Options include 'none', 'info', 'verbose', and 'verbose+sound'.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more details.
