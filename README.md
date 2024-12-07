# CSV Category Importer  

**CSV Category Importer** is a WordPress plugin that allows bulk importing of WooCommerce product categories from a CSV file. With support for nested categories, descriptions, and thumbnail images, this plugin simplifies managing complex category structures in WooCommerce stores.  

---

## 📋 Features  

- **Bulk Import Categories**  
  Import multiple categories in a single upload.  

- **Parent-Child Relationship Support**  
  Automatically assigns parent and child relationships based on the CSV file.  

- **Category Descriptions**  
  Add detailed descriptions for each category during import.  

- **Thumbnail Images**  
  Import thumbnail images using image URLs directly from the CSV.  

- **User-Friendly Interface**  
  Simple and intuitive admin page for uploading and managing imports.  

- **Error Handling**  
  Logs issues such as missing parent categories or invalid image URLs.  

- **Special Icons and Indications**  
  - ✅ Success notification for successful imports.  
  - ❌ Error notification for failed imports.  
  - ⚠️ Warnings for missing or incorrect data.  

---

## 🔧 Requirements  

- **WordPress Version**: 5.8 or higher  
- **WooCommerce Version**: 5.0 or higher  
- **PHP Version**: 7.4 or higher  

---

## 🛠️ Functions Used  

### WordPress Core Functions  

- `wp_insert_term()`  
  Creates new terms (categories) and assigns properties.  

- `get_term_by()`  
  Retrieves term information to establish parent-child relationships.  

- `term_exists()`  
  Checks if a term already exists before creating a new one.  

- `wp_handle_upload()`  
  Handles file upload processes securely.  

- `media_sideload_image()`  
  Downloads and attaches images to terms using URLs.  

### WooCommerce Functions  

- `set_term_meta()`  
  Adds meta data (e.g., thumbnail ID) to categories.  

### Custom Plugin Functions  

- `import_woocommerce_categories_from_csv()`  
  Processes the uploaded CSV file and creates categories based on the data.  

- `csv_import_page_html()`  
  Displays the plugin’s admin page interface.  

- `validate_csv_data()`  
  Validates the CSV format and required fields.  

- `generate_success_notice()`  
  Shows a success message after processing the CSV file.  

---

## 🛡️ Multiple Features  

### 🗂️ Nested Categories  
Easily create complex category hierarchies with parent and child relationships.  

### 🖼️ Thumbnail Management  
Assign thumbnails to categories using image URLs directly in the CSV.  

### 📊 CSV Validation  
Automatically detects and handles formatting errors in uploaded files.  

### 🌟 Admin Dashboard Integration  
Integrates seamlessly into the WordPress admin menu.  

### 📦 Compatibility  
Fully compatible with WooCommerce for online stores.  

---

## 🚀 Installation  

1. Download the plugin ZIP file.  
2. Log in to your WordPress admin dashboard.  
3. Go to **Plugins** → **Add New** → **Upload Plugin**.  
4. Upload the ZIP file and click **Install Now**.  
5. Activate the plugin.  

---

## 📋 CSV Format  

Your CSV file should follow this structure:  

```csv  
Category Name,Slug,Parent Category,Description,Thumbnail URL  
Google Pixel,google-pixel,Mobile Parts,Google Pixel Spare Parts,https://example.com/image.jpg  