# ASCII Art Converter - Web
[https://ascii.udav4ik.dev](https://ascii.udav4ik.dev)

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

## Statistics Dashboard
[https://ascii.udav4ik.dev/dashboard.html](https://ascii.udav4ik.dev/dashboard.html)

View real-time statistics about API usage:
- **Total Conversions**: All-time conversion count
- **Today's Conversions**: Daily activity with comparison to yesterday
- **Unique Users**: Number of unique IP addresses
- **Average Per Day**: 30-day average conversion rate
- **Charts**: Daily conversions and overall growth trends

**Real-time Updates**: The dashboard uses Server-Sent Events (SSE) for instant updates without page refresh.

## API Endpoint
  **For complete API documentation, see [API_GUIDE.md](API_GUIDE.md)**
