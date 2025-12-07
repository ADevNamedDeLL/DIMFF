# **DIMFF — Delete Image MetaData Fucking Fast**  
_A modern Windows desktop app for viewing, editing, and removing image metadata._

> **DIMFF** = **Delete Image MetaData Fucking Fast** — a clean, fast, modern EXIF editor & metadata cleaner.

<p align="center">
  <!-- Badges (placeholders) -->
  <img src="https://img.shields.io/badge/Project-DIMFF-black?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Platform-Windows-blue?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Framework-.NET%20WinForms-purple?style=for-the-badge" />
  <img src="https://img.shields.io/badge/License-MIT-green?style=for-the-badge" />
</p>

---

## ✨ Features

### 🔧 Metadata Cleaning
- Remove **all metadata** from images by re-encoding the bitmap.
- Save cleaned images:
  - **Overwrite original**
  - **Save as new file**

### 📝 Metadata Viewing & Editing
- Load, inspect, and modify:
  - EXIF  
  - TIFF  
  - GPS  
  - MakerNote  
  - Windows XP metadata fields  
- Edit all **ASCII-based EXIF tags**.
- Human-readable formatting for values:
  - Example: `ExposureTime: 1/60 (0.0167 s)`

### 🧠 Advanced Format Decoding
DIMFF fully understands:

- `ASCII`
- `SHORT`
- `LONG`
- `RATIONAL`
- `SRATIONAL`
- `BYTE` / `UNDEFINED` (raw fallback)

### 📚 Tag Dictionary
- Built-in EXIF TagName dictionary with **hundreds** of known IDs.

---


# ⚙️ Technical Details

| Component             | Description                                       |
|----------------------|----------------------------------------------------|
| **Language**          | C#                                                |
| **Framework**         | .NET WinForms                                     |
| **Image Handling**    | System.Drawing (GDI+)                             |
| **Metadata**          | Custom EXIF decoder & partial writer              |
| **Supported Formats** | JPG, JPEG, TIFF (full EXIF), PNG (limited)        |

---

# 📥 Installation

1. Download the latest **DIMFF** release from the **Releases** section.  
2. Extract the ZIP file.  
3. Run:

```text
DIMFF.exe
```
# 🚀 Usage

## Cleaning Metadata
1. Open **Clean Metadata** tab.  
2. Browse for an image.  
3. Click **Remove Metadata**.  
4. Save (overwrite or save-as).

## Viewing & Editing Metadata
1. Open **View & Edit Metadata** tab.  
2. Browse for an image.  
3. DIMFF loads and decodes metadata.  
4. Edit ASCII fields through the UI.  
5. Save changes.

---

# ⚠️ Limitations

- Binary EXIF fields (RATIONAL, SRATIONAL, UNDEFINED, MakerNotes, etc.)  
  → **Not editable** in the current version.  
- PNG metadata is not EXIF-based; only minimal reading/editing is possible.  
- GDI+ re-encoding may drop rare or unusual color profiles.  
- Some camera-specific MakerNotes may decode inconsistently.

---

# 📜 License

DIMFF is released under the **MIT License**.  
You may use, modify, and distribute freely under MIT terms.

## ❗ Additional Disclaimer

The authors and contributors of **DIMFF** are **not responsible for how this software is used**.  
This includes, but is not limited to:

- Removing metadata in ways that violate laws, regulations, or platform policies  
- Using the software for deceptive, malicious, or harmful purposes  
- Any data loss or file corruption resulting from misuse  

By using DIMFF, you agree that **you are solely responsible** for your actions and usage of this tool.

---

# 🙌 Credits

- Built in **C#** using **WinForms**.  
- EXIF tag dictionary inspired by public EXIF and TIFF specifications.  


