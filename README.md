# AIG Shares Outstanding Dashboard

This single-file, responsive HTML application displays the maximum and minimum shares outstanding for a given company, fetched from the SEC EDGAR API. It uses Tailwind CSS for styling and vanilla JavaScript for data fetching and dynamic content updates.

## Features

-   **Dynamic Data Display**: Fetches and displays the entity's common stock shares outstanding data.
-   **Max/Min Value Identification**: Highlights the maximum and minimum share values recorded after fiscal year 2020.
-   **Responsive Design**: Utilizes Tailwind CSS for a mobile-first, responsive layout.
-   **Configurable CIK**: Allows specifying a CIK via URL parameter to view data for different companies.
-   **Live Updates**: Updates the page content without a full reload when a new CIK is provided through the URL.

## Data Source

Data is sourced directly from the U.S. Securities and Exchange Commission (SEC) EDGAR API, specifically the `xbrl/companyconcept` endpoint for `dei/EntityCommonStockSharesOutstanding.json`.

### Initial Company (Default)

-   **Company**: American International Group (AIG)
-   **CIK**: 0000005272

## How to Run

1.  **Save the file**: Save the `index.html` content to a file named `index.html`.
2.  **Save `uid.txt`**: Ensure the `uid.txt` file is in the same directory as `index.html`.
3.  **Open in Browser**: Open `index.html` directly in your web browser.

## Usage

-   **Default View**: Simply open `index.html`. It will load data for American International Group (AIG) by default.
-   **View Another Company**: Append `?CIK=<your_cik_here>` to the URL to load data for a different company. For example, to view data for another company with CIK `0001018724`:
    `file:///path/to/index.html?CIK=0001018724`

    *Note: When fetching data for a CIK other than the default, the application uses a public CORS proxy (`api.allorigins.win`) to bypass potential cross-origin restrictions on client-side requests to the SEC API. This may affect performance or reliability based on the proxy service.*

## `uid.txt` Attachment

This project includes an attachment named `uid.txt`. As per instructions, this file is referenced in the `index.html` using an `<img>` tag. While `uid.txt` is a text file and typically not displayed as an image, it is included literally as instructed. You will likely see a broken image icon on the page if it doesn't contain valid image data.