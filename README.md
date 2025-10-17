# Sales Summary Dashboard

This project provides a simple, single-page web application to summarize sales data from a `data.csv` file. It's built with modern web standards, using HTML, JavaScript, and styled with Tailwind CSS for a responsive and clean user interface.

## Features

*   **Data Fetching:** Automatically fetches `data.csv` from the same directory.
*   **Sales Calculation:** Parses the CSV file, identifies the 'sales' column, and calculates the total sum of sales.
*   **Dynamic Display:** Shows the total sales in a prominent display area.
*   **Responsive Design:** Utilizes Tailwind CSS to ensure a good user experience across various device sizes.
*   **Error Handling:** Provides user feedback if the `data.csv` file is not found, malformed, or missing the 'sales' column.

## Setup and Usage

To run this application, you only need a web browser.

1.  **Save Files:** Ensure `index.html` and `data.csv` are in the *same directory*.
2.  **Open in Browser:** Simply open the `index.html` file in your preferred web browser (e.g., by double-clicking it).

The application will automatically load `data.csv`, calculate the total sales, and display it. The browser's title will also update to reflect the "Sales Summary" along with the current date.

### `data.csv` Format

The `data.csv` file is expected to be a comma-separated values file with a header row. It **must** contain a column named `sales`. Example:

```csv
product,sales,region
Widget A,123.45,North
Gadget B,678.90,South
Product C,345.00,East
```

Non-numeric values in the 'sales' column will be skipped with a warning in the browser's console.

## Technologies Used

*   **HTML5:** For the core structure of the web page.
*   **JavaScript (ES6+):** For data fetching, parsing, and dynamic content updates.
*   **Tailwind CSS:** A utility-first CSS framework for rapid UI development and responsive design.

## Project Structure

```
.
├── index.html
├── data.csv  (provided by the user, expected in the same directory)
└── README.md
└── LICENSE
```

## Contributing

This project is a small, self-contained demonstration. While direct contributions are not expected for this specific setup, feel free to adapt and expand upon the code for your own projects.

---
**Note:** This application fetches `data.csv` using a relative path. For security reasons, modern browsers might restrict `file://` URLs from making `fetch` requests to local files directly due to CORS policies. If you encounter issues (e.g., "CORS error"), serving the files via a simple local HTTP server (e.g., `python -m http.server` from the directory) is recommended.