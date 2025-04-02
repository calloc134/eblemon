# eblemon

A command-line tool to download images from a specified web page.  
The program reads configuration from a TOML file ("eblemon.toml") and uses it to set up download directories and host settings.

## Features

- Reads settings from "eblemon.toml", including download base directory and host URL.
- Prompts the user for the target page URL.
- Retrieves metadata (such as title and total pages) from the specified URL.
- Creates a download directory with a sanitized version of the page title.
- Downloads images sequentially from subsequent pages and displays a progress bar.

## Usage

1. Configure the "eblemon.toml" file with `base_ebook_host` and `download_base_dir`.

```toml
base_ebook_host = "https://example.com"
download_base_dir = "/path/to/download/directory"
```

- `base_ebook_host`: The base URL of the host from which images will be downloaded.
- `download_base_dir`: The directory where images will be saved.

2. Run the tool.
3. When prompted, input the URL of the target page.
4. The tool will fetch the required metadata, skip the initial non-content page, and download the images accordingly.
