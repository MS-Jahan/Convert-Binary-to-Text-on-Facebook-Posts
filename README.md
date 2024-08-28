
# Convert Binary to Text on Facebook Posts

This Tampermonkey script automatically converts binary text to readable text on Facebook posts. It runs every second to handle dynamically loaded content, ensuring that binary text is converted properly.

## Features

- **Automatic Conversion**: Converts binary strings to readable text.
- **Dynamic Content Handling**: Runs every second to process new or dynamically loaded content.
- **URL Specific**: Applies only to Facebook posts URLs with the format `https://www.facebook.com/*/posts/*`.

## Installation

To use this script, follow these steps:

1. **Install Tampermonkey**: Ensure you have the Tampermonkey extension installed in your browser. You can download it from [Tampermonkey's official website](https://www.tampermonkey.net/).

2. **Create a New Script**:
   - Open the Tampermonkey dashboard.
   - Click on the "Create a new script" button.

3. **Paste the Script**:
   - Replace the default template with the script provided in the repository.

4. **Save and Enable**:
   - Save the script and ensure it is enabled.

## Adapting the Script for Other Websites

To use this script on other websites, you need to modify the `@match` parameter in the script's metadata. This parameter determines which URLs the script will run on.

1. **Find the `@match` Line**:
   - Locate the `@match` line in the script's metadata block.

2. **Update the URL Pattern**:
   - Change the URL pattern to match the desired website. For example:
     - To match URLs on `https://example.com/page/*`, use `https://example.com/page/*`.
     - To match URLs on `https://www.example.com/`, use `https://www.example.com/*`.

3. **Save the Script**:
   - After updating the `@match` parameter, save the script in Tampermonkey.

### Example

If you want to adapt the script for a different website with the URL pattern `https://www.example.com/posts/*`, you would update the `@match` line as follows:

```javascript
// @match        https://www.example.com/posts/*
```

## Usage

- **URL Pattern**: This script is designed to run on URLs matching the pattern specified in the `@match` parameter. Ensure you are visiting pages that fit this pattern for the script to be active.
- **Dynamic Content**: The script will automatically handle new content added to the page, such as additional posts or comments loaded after interactions like "See More."

## Troubleshooting

- **Script Not Running**: Ensure that the URL pattern matches the current page URL.
- **Binary Text Not Converting**: Check that the text content contains only `0`s and `1`s. The script may not work if the binary data is formatted differently.

## Contributions

Feel free to fork the repository and submit pull requests if you have improvements or fixes.
