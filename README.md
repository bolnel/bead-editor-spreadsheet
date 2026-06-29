# Bead Pattern Template

Custom rocaille bead pattern editor in Google Sheets. The template dimensions are 120*26 beads, could be used for collars or bracelets.

- **Bead Pattern Template.xlsx** – spreadsheet template with required formatting and structure
- **BeadPattern.gs** – Google Apps Script that powers the automation and menu system

---

## Installation

### 1. Create a Google Sheets copy

Upload **Bead Pattern Template.xlsx** to Google Drive and open it with **Google Sheets**.

---

### 2. Add the script

1. Open the spreadsheet.
2. Go to **Extensions → Apps Script**.
3. Delete any existing code in the editor (for example `Code.gs`).
4. Copy the contents of **bead-editor-template-script.js** from this repository and paste it into the editor.
5. Click **Save**.

---

### 3. Authorize the script

The script requires permission to modify the spreadsheet. This is a one-time setup per spreadsheet.

1. Save the script.
2. Return to the spreadsheet and refresh the browser tab (or close and reopen it).
3. If prompted, review and grant permissions:
   - Click **Review permissions**
   - Select your Google account
   - If you see *"Google hasn't verified this app"*, click **Advanced**, then **Go to project (unsafe)** (this is expected for personal scripts)
   - Click **Allow**

If the **Bead pattern** menu does not appear after refreshing, open **Extensions → Apps Script**, select any function (for example `countAddLetters`) and click **Run** once. Then refresh the spreadsheet again.

---

> **Note:** Each copy of the template contains its own Apps Script project. As a result, the script must be authorized once for every new copy of the spreadsheet. This is a normal Google Apps Script security requirement.

---

### 4. Reload the spreadsheet

After authorization, refresh the spreadsheet.

A new menu named **Bead pattern** will appear in the top toolbar.

---

## Using the system

The **Bead pattern** menu provides all main actions:

### Top-level actions
- **Count + add letters** – outputs the count of each bead into Palette. Writes the letters for each color into Pattern
- **Populate palette** – extracts new colors from Pattern into Palette. Run when you finished designing the pattern. Rows in Palette can be rearranged afterwards. Running this function again after design changes will add the colors that aren't in Palette yet.
- **Clear pattern text** – removes letters from Pattern while keeping colors
- **Swap colors** – Put the new colors as background in the Swapper column cells. Running this function will replace the original colors with the new ones

### Tools (singular functions)
- Set grid (5×5)
- Count colors
- Add letters in Palette letter column (ABCDE...)
- Render letters in Pattern

---

## Updating

To update the script:

1. Open **Extensions → Apps Script**
2. Replace the script with the latest version from this repository
3. Click **Save**
4. Refresh the spreadsheet

Your data and formatting will remain unchanged.
