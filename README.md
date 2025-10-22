# SEC Entity Common Stock Shares Outstanding Viewer

This single-file, responsive web application displays the maximum and minimum common stock shares outstanding for a given company, fetched directly from the SEC EDGAR API.

## Features

*   **Dynamic Data Fetching**: Retrieves company shares outstanding data using the SEC EDGAR API.
*   **Responsive Design**: Built with Tailwind CSS for optimal viewing across various devices.
*   **Interactive CIK Input**: Automatically loads data for Cintas (CIK: `0000723254`) by default. Users can specify a different CIK via a URL query parameter (e.g., `index.html?CIK=0001018724`).
*   **Data Filtering**: Filters data to show only entries with fiscal years (`fy`) greater than 2020 and valid numeric values.
*   **Max/Min Display**: Clearly highlights the maximum and minimum shares outstanding along with their respective fiscal years.

## How to Use

1.  **Open `index.html`**: Simply open the `index.html` file in your web browser.
2.  **Default View**: The application will automatically fetch and display data for Cintas (CIK: `0000723254`).
3.  **Specify a Different CIK**: To view data for another company, append `?CIK=` followed by the 10-digit CIK to the URL in your browser's address bar. For example:
    `file:///path/to/your/index.html?CIK=0001018724`
    (Replace `file:///path/to/your/index.html` with the actual path to your file, or host it on a web server.)

## Technical Details

*   **Frontend**: HTML, Tailwind CSS, JavaScript.
*   **Data Source**: SEC EDGAR API (`https://data.sec.gov/api/xbrl/companyconcept/`).
*   **Proxy**: Utilizes `https://api.allorigins.win/` as a CORS proxy for client-side API requests.
*   **User-Agent**: For client-side `fetch` requests, the `User-Agent` header is typically managed by the browser or the proxy. For server-side applications interacting with SEC EDGAR, it's crucial to set a descriptive `User-Agent` (e.g., `YourAppName/1.0 (your-email@example.com)`) as per SEC guidance to ensure proper request attribution and avoid IP blocking.

## Development

To run this locally, save the `index.html` file and open it in any modern web browser.

## License

This project is licensed under the MIT License. See the `LICENSE` file for full details.