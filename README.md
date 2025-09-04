# GhostHarvester - Obfuscated Version

[![Version](https://img.shields.io/badge/version-2.2.4-blue.svg)](https://github.com/vsmz4laj7n/GhostHarvester)
[![Python](https://img.shields.io/badge/python-3.12+-green.svg)](https://www.python.org/downloads/)

This is the **obfuscated version** of GhostHarvester - An advanced Telegram data analysis and extraction tool. The source code is protected using CodeEnigma obfuscation technology for enhanced security.

**The access price for this tool (full usage rights, excluding support and updates) is 100 USD (100 USDT - Crypto = 2,500,000 VND).**

## 🔒 Obfuscation Features

- **Source Code Protection**: Code is obfuscated and secured
- **Runtime Security**: Secure bytecode execution with CodeEnigma runtime
- **Full Functionality**: All features of the original GhostHarvester
- **Easy Installation**: Automated setup with dependency management

## 📋 Requirements

- **Python 3.12+** (Required)
- **Build Tools**: gcc, make (Linux/macOS) or Visual Studio Build Tools (Windows)
- **Telegram API Credentials** (api_id and api_hash from [my.telegram.org](https://my.telegram.org))
- **Valid Phone Number** (for Telegram authentication)

## 🚀 Quick Setup

### Option 1: Automated Installation (Recommended)

1. **Run the automatic installer:**
   ```bash
   python install.py install
   ```

   This will:
   - Create a virtual environment
   - Install all dependencies
   - Build the obfuscated extension
   - Install the package

### Option 2: Manual Installation

1. **Create a virtual environment:**
   ```bash
   python3.12 -m venv venv
   source venv/bin/activate  # Linux/macOS
   # or
   venv\Scripts\activate     # Windows
   ```

2. **Install dependencies:**
   ```bash
   pip install cython setuptools wheel
   pip install -r requirements.txt
   ```

3. **Build and install:**
   ```bash
   python setup.py build_ext --inplace
   pip install -e .
   ```

## ⚙️ Configuration

1. **Copy and edit the configuration file:**
   ```bash
   cp config_real.ini my_config.ini
   ```

2. **Edit `my_config.ini` with your details:**
   ```ini
   [CONFIGURATION]
   api_id=YOUR_API_ID
   api_hash=YOUR_API_HASH
   phone_number=+YOUR_PHONE_NUMBER
   data_path=/path/to/your/data/folder/
   ```

3. **Obtain Telegram API credentials:**
   - Visit [my.telegram.org](https://my.telegram.org)
   - Log in with your phone number
   - Go to "API development tools"
   - Create a new application to obtain `api_id` and `api_hash`

## 🧪 Testing

### Test Installation

```bash
# Check help command
python install.py test

# Or test manually
source venv/bin/activate
python -m ghavest --help
```

### Test with Configuration

```bash
# Test with your configuration
python -m ghavest connect --config my_config.ini
```

## 🚀 Usage

After installation, activate the virtual environment:

**Linux/macOS:**
```bash
source venv/bin/activate
```

**Windows:**
```bash
venv\Scripts\activate
```

### Available Commands

```bash
# Display help
python -m ghavest --help

# Connect to Telegram (initial setup)
python -m ghavest connect --config my_config.ini

# Load groups and members
python -m ghavest load_groups --config my_config.ini

# Download messages
python -m ghavest download_messages --config my_config.ini

# Listen for live messages
python -m ghavest listen --config my_config.ini

# Generate report
python -m ghavest report --config my_config.ini

# Export data
python -m ghavest export_text --config my_config.ini
python -m ghavest export_html --config my_config.ini

# Analyze data
python -m ghavest analyze --config my_config.ini

# Display statistics
python -m ghavest stats --config my_config.ini
```

## 🔧 Advanced Usage

### Manual Build Process

If you need to rebuild the obfuscated code:

```bash
# Clear previous builds
python install.py clean

# Rebuild
python setup.py build_ext --inplace
pip install -e .
```

### Development Mode

For development with the obfuscated version:

```bash
# Install in development mode
pip install -e .

# Make changes and reinstall
pip install -e . --force-reinstall
```

## 📁 Directory Structure

```
obfuscate/
├── ghavest/                    # Obfuscated package
│   ├── core/                  # Core functionality (obfuscated)
│   ├── database/              # Database management (obfuscated)
│   ├── modules/               # Processing modules (obfuscated)
│   └── ...                    # Other modules (obfuscated)
├── codeenigma_runtime.pyx     # Runtime extension source
├── codeenigma_runtime.so      # Compiled extension
├── setup.py                   # Build configuration
├── install.py                 # Automated installer
├── requirements.txt           # Dependencies
├── config_real.ini            # Configuration template
├── pyproject.toml            # Project metadata
└── README.md                 # This file
```

## 🐛 Troubleshooting

### Common Issues

1. **Python Version Error:**
   ```
   Error: Python 3.12+ is required
   ```
   **Solution:** Install Python 3.12 or higher

2. **Missing Build Dependencies:**
   ```
   error: Microsoft Visual C++ 14.0 is required
   ```
   **Solution:** 
   - **Windows:** Install Visual Studio Build Tools
   - **Linux:** Install `build-essential`: `sudo apt-get install build-essential`
   - **macOS:** Install Xcode Command Line Tools: `xcode-select --install`

3. **Cython Not Found:**
   ```
   ModuleNotFoundError: No module named 'Cython'
   ```
   **Solution:** `pip install cython`

4. **Import Error:**
   ```
   ImportError: No module named 'codeenigma_runtime'
   ```
   **Solution:** Rebuild the extension:
   ```bash
   python setup.py build_ext --inplace
   pip install -e .
   ```

5. **Virtual Environment Issue:**
   ```
   Error: No such file or directory: venv/bin/pip
   ```
   **Solution:** Recreate the virtual environment:
   ```bash
   rm -rf venv
   python3.12 -m venv venv
   ```

## 🔒 Security Notes

- This is the obfuscated version with advanced code protection
- Source code is obfuscated and protected against reverse engineering
- Runtime execution is secured via CodeEnigma
- All functionality is identical to the original version

---

**Safe and Secure! 🔒**
