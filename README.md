# ASCII Art Converter - Web
[https://ascii.udav4ik.dev/api/convert](https://ascii.udav4ik.dev/api/convert)
A minimalistic web interface for converting images to ASCII art with full 24-bit RGB color support.

## How to Use

1. **Upload an Image**: Drag and drop or click to select
2. **Adjust Settings**: 
   - Width/Height (characters)
   - Edge Detection (optional)
   - Terminal Colors (enable for colored output)
3. **Convert**: Click the "Convert" button
4. **View Results**:
   - **Plain Tab**: Standard ASCII art (no colors)
   - **Colored Tab**: Web-friendly colored version
   - **Terminal Tab**: Raw ANSI codes for terminal use

## Output Formats

### Plain ASCII
Standard ASCII art without any colors or special formatting.

### Colored Web View
ASCII art with colors applied via HTML spans - perfect for web display and easy to read.

### Terminal Output
  **Some browsers may not handle ANSI escape codes properly when copying text and displaying it on the page.**
  - **Copy Raw**: Copies actual ANSI escape bytes (wont show colors if just pasted into terminal)
  - **Copy Escaped**: Copies visible `\x1b` sequences (will show colors if is pasted inside echo"|")
  - **Download**: Saves file with raw ANSI codes - run `cat filename.txt` in terminal to view with colors.


## API Endpoint

**For complete API documentation, see [API_GUIDE.md](API_GUIDE.md)**

### POST `https://ascii.udav4ik.dev/api/convert`

**Response:**
```json

{
  "ascii": "ASCII art output here...",
  "edge_threshold": null,
  "filename": "name.png",
  "has_colors": false,
  "height": 100,
  "width": 100
}
```



---

