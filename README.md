# 🛡️ MagnusR9 – Open-Source Web & WordPress Utilities

Lightweight, zero-tracking, client-side browser extensions (Manifest V3) and modernized WordPress utility forks maintained by **MagnusR9**.

---

## 🌐 Chrome Web Store Extensions (Manifest V3)

### 1. Media Deduplicator & Broken Image Auditor (`v1.0.2`)
* **8x8 Perceptual Visual Hashing (aHash):** Detects visually identical duplicate images on any webpage or WordPress Media Library, even when files are renamed or scaled (`-150x150`, `-scaled`, `-1`).
* **Broken Link (404) & Missing Alt Detector:** Instant visual DOM audit with 1-click CSV export.

### 2. Copy All URLs, Tab Exporter & Duplicate Closer (`v1.0.0`)
* **Zero-Quota Manifest V3 Architecture:** Unlike legacy extensions that fail above 45 tabs due to `chrome.storage.sync` 8KB limits, this tool copies 200+ tabs instantly as **Plain Text, Markdown (`[Title](url)`), CSV, or JSON**.
* **1-Click Duplicate Tab Closer & Batch URL Opener.**

### 3. Export SVG with Computed Styles & Code Copy (`v1.0.0`)
* **Recursive CSS Style Inliner:** Reads `window.getComputedStyle()` (`fill`, `stroke`, `opacity`) and bakes styles directly into exported `<svg>` nodes so vectors never turn black in Figma, Illustrator, or React.

---

## 🔌 WordPress.org Plugin Forks (PHP 8.3 & WP 7.x Patched)

### 4. MagnusR9 Media Deduplicator (`v2.0.0` – GPLv2+)
* **Shared Physical File Protection (Critical Data-Loss Fix):** Prevents `wp_delete_attachment()` from deleting the physical image file on disk when multiple attachment posts share the same `_wp_attached_file` path (e.g., after *WP All Import* runs).
* **WooCommerce Product Gallery Re-Linking:** Automatically updates `_thumbnail_id` and `_product_image_gallery` references before removing duplicates.
* **1-Click Smart Bulk Clean Toolbar.**

### 5. MagnusR9 Regions for WP Job Manager (`v2.0.0` – GPLv2+)
* **Fixes jQuery 3.x Frontend Crash:** Replaces removed `$(document).on('ready')` and unguarded `.chosen()` calls in `main.js` for modern Select2 compatibility.
* **PHP 8.2/8.3/8.4 & WP 6.7+ Ready:** Fixes `_load_textdomain_just_in_time` notice, removes unsafe `extract()`, and adds null-safe `WP_Term` checks.
* **100% Drop-In Compatible:** Preserves existing `job_listing_region` and `resume_region` taxonomies for themes like *Jobify* and *Listify*.
