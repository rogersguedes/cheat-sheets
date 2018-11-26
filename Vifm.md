### Vifm Sheet

1. `Ctrl+w` + `o`: close current pane;
2. Copy File: `yy`
3. Paste: `p`
4. Create new folder: `:mkdir <dirname>`
5. Display/Hide hidden files: `zo` / `za`
6. Renaming a file: Move the cursor to the file. Press `cw` (first `c` then `w`) and type the new name. Alternatively, press `cW` if you want to maintain the extension.
7. Deleting a single file: put the cursor over the file you want to delete and press `dd`.
8. Deleting multiple files: press `v`, select the files you want to delete using `j` or `k` (or directional arrows) and, when all undesired files are selected, press `dd`.

#### Commands

1. `:split`: split current pane horizontally.
2. `:vsplit`: split current pane vertically.
3. `:![bin] %c`: runs the `[bin]` passing current select file as parameter.

### References

1. https://fossbytes.com/vifm-beginner-tutorial-file-manager-gnu-linux/
2. https://wiki.vifm.info/index.php/Quickstart_Tutorial