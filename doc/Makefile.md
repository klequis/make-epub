
## All commands in makefile that include "epub"

- `EPUB_ARGS = --template templates/epub.html --epub-cover-image $(COVER_IMAGE)`
- `EPUB_DEPENDENCIES = $(BASE_DEPENDENCIES)`
	- This looks like the command line to run
- `epub: $(BUILD)/epub/$(OUTPUT_FILENAME).epub`
	- This has multiple commands that need to be analyzed.