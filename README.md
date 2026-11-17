### Usage
```bash
AXIONRU_URL="https://github.com/andrey167/AxionRu.git"
AXIONRU_DIR="$(pwd)/.axionru_tmp"

rm -rf "$AXIONRU_DIR"
git clone --depth=1 "$AXIONRU_URL" "$AXIONRU_DIR" || {
    echo "ERROR: Failed to clone AxionRu!"
    rm -rf "$AXIONRU_DIR"
    exit 1
}

# Copy translations into Android sources, replacing existing files
cp -af "$AXIONRU_DIR/." "$(pwd)/"

rm -rf "$AXIONRU_DIR"
```
