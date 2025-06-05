# Basic Google Maps Scraper

**Description:**  
An n8n workflow that scrapes Google Maps for “cafe” listings in Bangkok using the Apify API and appends results to a Google Sheet.

**Prerequisites:**  
- n8n instance (v1.0+).  
- Apify API token with the “google-maps-with-contact-details” actor enabled.  
- Google Sheets OAuth2 credentials to write to your target spreadsheet.  

**Usage:**  
1. Import `Basic_Google_Maps_Scraper.json` into n8n.  
2. In the **HTTP Request** node, replace `apify_api_vP2sFh6bZ2lSwsfsbGPMnZWJNdGaIl1dLe5U` with your own Apify token.  
3. In the **Google Sheets** node, select or configure the OAuth2 credential that has edit access to your sheet.  
4. In the **Schedule Trigger** node, adjust the schedule if needed (defaults to weekly on Friday at 06:00 UTC).  
5. Activate and run the workflow. Scraped data (title, address, phone, reviews, URL, etc.) will append to the specified sheet.

**File Structure:**  
- `Basic_Google_Maps_Scraper.json` (n8n workflow definition)  
- `README.md` 
