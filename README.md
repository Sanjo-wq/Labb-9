# Employee XML Data Viewer

A modern, responsive web application designed to parse XML data containing employee information and present it in an interactive, clean tabular format.

## Project Structure
- `employees.xml` - XML data file storing employee records (ID, Name, Gender, Department, Position, Email, Salary, Joining Date, Status).
- `index.html` - Complete web application with DOM parser, responsive table, summary cards, search filter, and column sorting.

## Key Features
1. **XML Parsing (`DOMParser`)**: Automatically parses standard XML structures including elements (`<name>`, `<salary>`, etc.) and attributes (`id="EMP101"`).
2. **Three Loading Options**:
   - **Upload Local XML**: Pick any custom `.xml` file from your computer using the HTML5 `FileReader` API (works under any protocol, including `file://`).
   - **Fetch `employees.xml`**: Dynamically requests `employees.xml` over HTTP/HTTPS.
   - **Built-in Sample**: Instant load without external dependencies.
3. **Interactive Table Features**:
   - Multi-column search filter (matches ID, Name, Department, Position, or Email).
   - Department category dropdown filter with live item counts.
   - Click-to-sort on any column (ascending and descending).
   - Summary statistics cards (total employees, department count, average salary, and active ratio).
   - XSS sanitization helper for safe rendering of XML text content.

## How to Run

### Method 1: Direct File Open (Easiest)
Simply double-click [index.html](file:///C:/Users/sanjo/.gemini/antigravity/scratch/employee_xml_viewer/index.html) or open it directly in any modern web browser (Edge, Chrome, Firefox).

### Method 2: Local HTTP Server (Optional)
If you want to test network `fetch()` requests directly:
```powershell
cd "C:\Users\sanjo\.gemini\antigravity\scratch\employee_xml_viewer"
python -m http.server 8000
```
Then visit `http://localhost:8000` in your web browser.
