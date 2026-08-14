# DIMFF — Delete Image MetaData Fucking Fast

A modern Windows desktop application for viewing, editing, and removing image metadata with a simple and efficient workflow.

**DIMFF** stands for **Delete Image MetaData Fucking Fast**. It is designed as a lightweight EXIF metadata viewer, editor, and cleaner for users who want direct control over the metadata stored inside their images.

<p align="center">
  <img src="https://img.shields.io/badge/Project-DIMFF-black?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Platform-Windows-blue?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Framework-.NET%20WinForms-purple?style=for-the-badge" />
  <img src="https://img.shields.io/badge/License-MIT-green?style=for-the-badge" />
</p>

---

## Features

### Metadata Cleaning

DIMFF can remove embedded metadata from supported images by re-encoding the image.

- Remove image metadata in a single operation.
- Overwrite the original image.
- Save the cleaned image as a separate file.
- Designed for fast and straightforward metadata removal.

### Metadata Viewing and Editing

Inspect and modify metadata directly from the application.

Supported metadata includes:

- EXIF
- TIFF
- GPS
- MakerNote
- Windows XP metadata fields

ASCII-based EXIF fields can be edited through the interface.

Metadata values are displayed in a human-readable format where applicable.

Example:

```text
ExposureTime: 1/60 (0.0167 s)
```

### EXIF Data Decoding

DIMFF includes a custom EXIF decoder capable of handling several common TIFF/EXIF data types:

- ASCII
- SHORT
- LONG
- RATIONAL
- SRATIONAL
- BYTE
- UNDEFINED

Unsupported or raw binary values can be displayed using a fallback representation rather than being silently discarded.

### Built-in Tag Dictionary

DIMFF includes a built-in EXIF tag dictionary containing hundreds of recognized tag identifiers, making metadata easier to understand without requiring users to manually interpret numeric tag IDs.

---

## Technical Details

| Component | Description |
|-----------|-------------|
| **Language** | C# |
| **Framework** | .NET WinForms |
| **Image Processing** | System.Drawing / GDI+ |
| **Metadata Processing** | Custom EXIF decoder and partial metadata writer |
| **Supported Formats** | JPG, JPEG, TIFF, PNG |
| **EXIF Support** | Full reading for supported JPEG/TIFF EXIF structures |
| **PNG Support** | Limited metadata support |

---

## Installation

1. Download the latest DIMFF release from the GitHub **Releases** section.
2. Extract the downloaded archive.
3. Launch the application:

```text
DIMFF.exe
```

No additional configuration is required for the portable release.

---

## Usage

### Cleaning Image Metadata

1. Open the **Clean Metadata** tab.
2. Select the image you want to process.
3. Click **Remove Metadata**.
4. Choose whether to overwrite the original file or save the cleaned image as a new file.

### Viewing and Editing Metadata

1. Open the **View & Edit Metadata** tab.
2. Select an image.
3. DIMFF reads and decodes the available metadata.
4. Review the detected EXIF and TIFF fields.
5. Modify supported ASCII-based fields when required.
6. Save the changes.

---

## Limitations

DIMFF is actively developed and currently has several limitations.

- Binary EXIF fields such as `RATIONAL`, `SRATIONAL`, and `UNDEFINED` are currently read-only.
- MakerNote data is not currently editable.
- PNG metadata handling is limited because PNG does not use the same EXIF structure as JPEG and TIFF.
- GDI+ re-encoding can remove or alter uncommon color profiles.
- Some camera-specific MakerNote structures may not decode consistently.
- Metadata support varies depending on the image format and the way the original file was created.

---

## License

DIMFF is released under the **MIT License**.

You are free to use, modify, distribute, and include the software in other projects, subject to the terms and conditions of the MIT License.

---

## Disclaimer

DIMFF is provided as a utility for legitimate image-management, privacy, development, testing, and metadata-processing purposes.

The authors and contributors are not responsible for how the software is used.

This includes, but is not limited to:

- Removing metadata in violation of applicable laws or regulations.
- Removing metadata in violation of a platform's policies or requirements.
- Using the software for deceptive, malicious, or otherwise harmful purposes.
- Data loss, file corruption, or unintended modifications resulting from improper use.
- Any consequences resulting from modifying or removing information embedded within an image.

Users are responsible for ensuring that their use of DIMFF complies with applicable laws, regulations, licenses, and third-party policies.

---

## Credits

- Developed in C# using .NET WinForms.
- Image processing is handled through System.Drawing and GDI+.
- EXIF decoding and metadata handling are implemented using custom code.
- The EXIF tag dictionary is based on publicly available EXIF and TIFF specifications.

---

## Project Status

DIMFF is an actively developed project.

The current implementation focuses on fast metadata removal, practical EXIF inspection, and basic editing capabilities. Additional metadata formats, data types, and writing capabilities may be introduced in future releases.
