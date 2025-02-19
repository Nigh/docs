- [[Nov 25th, 2021]]
  id:: a7a7603c-f4f2-49ab-a9c5-ca78c41b07db
  **Beta 0.5.1**
  Desktop app download link: https://github.com/logseq/logseq/releases/tag/0.5.1
	- [[Fixed issues]]
		- Changes are not saved to files when using Logseq and OneDrive on multiple computers
			- **We strongly encourage you to upgrade to the latest version to avoid any data loss.**
		- Markdown blockquote syntax parsing not backward compatible
		- `Contents` is not considered a "Built-in page" for Graph view
- [[Nov 24th, 2021]]
  id:: 619e5440-72c1-4d04-bf4b-dd911f1c69b3
  **Beta 0.5.0**
  Desktop app download link: https://github.com/logseq/logseq/releases/tag/0.5.0
	- [[Thanks]]
		- [[Gabriel Horner]]
			- Add datalog console extension in dev
			- Fix GitHub CI
		- [[David Whittington]]
			- Support #Arweave URLs for links and images
		- [[Peng Xiao]]
			- Custom macro click issue
	- [[Fixed issues]]
		- [[Windows]] desktop app is finally signed
		- Clean block's referenced old orphaned pages when saving it
		- Can't open a new graph on Linux
		- Git Autocommit not working
		- Can't open external links like Zotero and mail clients
		- Don't create empty pages for alias and tags page properties
		- Auto-complete doesn't vanish after /current time
		- Slow parsing on base64 image link
		- Query filters like `and`, `or` are case sensitive
		- Can't rename pages with nested titles
		- Remove space when showing template popup
		- All Pages view lists all of the images
		- Sometimes shortcuts stopped working
		- `[[` doesn't trigger auto-complete for non-english input methods
	- [[Enhancement]]
		- Convert highlighted word to a link when pasting a URL
		- Save a backup file to `logseq/bak` if writes failed (EBUSY lock)
		- Separate plugins and themes in the marketplace
		- Create today's page when redirect to the home or scrolling to the top of journals
		- Jump to the end of page ref after pressing Enter
		- Avoid press enter at empty page-ref
- [[Nov 19th, 2021]]
  **Beta 0.4.9**
  Desktop app download link: https://github.com/logseq/logseq/releases/tag/0.4.9
	- [[Fixed issues]]
		- Empty graph view
		- Shortcuts can be repeated sometimes
- [[Nov 18th, 2021]]
  id:: 8590ee9b-3f85-40cc-954d-857715503802
  **Beta 0.4.7**
  Desktop app download link: https://github.com/logseq/logseq/releases/tag/0.4.7
	- [[Thanks]]
		- [[Devon Zuegel]]
			- Enhance shortcut tooltips
	- [[Fixed issues]]
		- Rename page references when merging pages
		- Code block indentation
		- Block id not persisted when copy block embed
		- Linked references missing in the right sidebar
		- Make sure blocks have the same format when dragging to another page
		- Check for update
	- [[Enhancement]]
		- Toggle displaying shortcut tooltips on settings
			- ![CleanShot 2021-11-18 at 10.33.24.png](../assets/CleanShot_2021-11-18_at_10.33.24_1637202815754_0.png)
		- Display a warning if a block's content include multiple lists or headings
	- [[Breaking Changes]]
		- Deprecate both Ctrl/Cmd+u for searching and  `Ctrl/Cmd+Shift+u` for search in page, use `Ctrl/Cmd+k` and `Ctrl/Cmd+Shift+k` instead.
- [[Nov 16th, 2021]]
  id:: 38a7f160-5dbb-4ab0-8556-5e45cd15144a
  **Beta 0.4.6**
  Desktop app download link: https://github.com/logseq/logseq/releases/tag/0.4.6
	- [[Thanks]]
		- [[Devon Zuegel]]
			- Add more content-aware classes to textarea for a more WYSIWYG experience
			- Show default home instead of journals in side bar
			- Polish cards
			- Rename "page emoji" to "page icons"
				- This PR renames the page property `emoji` to `icon`, which is a more typical and more flexible name.
		- [[Peng Xiao]]
			- Add page & block ref to search item
			- Add back haschild attribute
	- [[Fixed issues]]
		- Navigating to a page through search caused Logseq to crash to a blank screen
		- Rename page should delete the old page name from search
		- Graphs disappeared (not data-loss) after restarting the app
		- Backspace can't move to previous block if it's a embed block
		- Cycle todos will not deselect the blocks
		- Git still commits even if it's toggled off on settings
		- Pages with "." in the title do not show Hierarchy at the bottom
		- Line starting with - will be disappear after exit editing
		- Cannot edit deadline/schedule using date picking panel
		- Ordered list can't be shown in reference list
		- Drag and Drop inconsistently not working
		- Alt-dragging a bullet to an indented position will create multiple empty bullet
		- Import JSON from Roam has trouble with certain code block syntax
		- No more auto-complete if the cursor moves back to [[]]
		- Empty path when importing roam's json
		- Renaming namespace page will update all its children's links
		- Page-ref replacement if non-slash in path
	- [[Enhancement]]
		- Merging pages when renaming one page to the name of another page
		- Add copy block embed(s)
		- Delay query for linked references
			- Editing the main page should be fast no matter how many linked references it has
		- Cycle todos support cmd+enter
		- Display a warning if config.edn is invalid
		- Don't add another set of (()) when copy block ref to embed
		- Remove built-in properties from search result
		- When depth level > 3, the breadcrumb displays an ellipsis
- [[Nov 10th, 2021]]
  id:: 45fc2d43-4154-4f20-ad60-c3039e35256d
  **Beta 0.4.5**
  Desktop app download link: https://github.com/logseq/logseq/releases/tag/0.4.5
	- [[Features]]
		- Move selected blocks up/down (Ctrl/Cmd + Shift + UP/DOWN)
		- `All pages` support batch delete, search, journals filter and remove orphaned pages
		  collapsed:: true
			- ![CleanShot 2021-10-23 at 00.06.33.png](../assets/CleanShot_2021-10-23_at_00.06.33_1634918821593_0.png)
		- Persist right sidebar state
		- [[Shortcuts]]
			- `g t` to go to tomorrow's page
			- `g p` to go to the previous journal
			- `g n` to go to the next journal
		- `custom.js` support
			- See more at https://github.com/logseq/logseq/pull/2943
	- [[Thanks]]
		- [[Devon Zuegel]]
			- Enhance: add hotkeys for open file in directory (`o d`) / default app (`o f`)
			- Emoji page identifiers + sidebar tweaks
			- Custom editor command trigger
				- New configuration option `:editor/command-trigger`
					- e.g. To use `\` instead of `/` for commands trigger, add `:editor/command-trigger "\\"` to `config.edn`.
		- [[Andelf]]
			- Wrong delta pos when change to empty marker
			- fix: pos and space when cycling marker in header
		- [[Seth]]
			- Update readme to include platform specific docker instructions
		- [[GoldinGuy]]
			- Add time wrapper for scheduled/deadline
		- [[Yongqinchuan Du]]
			- Fix code block wide mode toggle
		- [[Peng Xiao]]
			- Fix: notification wrapper blocks user from interacting with the main area
	- [[Fixed issues]]
		- Failed to import roam research's json
		- Both `Copy as` and `Export page` should be fast now
		- Display the below plus button when zoom in
		- Several issues when renaming namespace pages
		- Marking task from "Now" to "Done" lost tracking time duration data
		- Timetracking for now->later on repeated task
		- Timetracking support seconds now
		- Logbook related issues
		- Files not saved when onboarding if canceled the file picker
		- Encrypted page for revert history version by git
		- Decrypt file content when diff
		- Broken image preview in the right sidebar
		- Fix slash command clashes with Org-mode italics
		- Org page reference allows different page-name and label
		- Blank screen on preview card with empty card
		- Clear block content when auto-complete page references
		- Insert page attributes instead of block property when creating and renaming a page
		- Latex can't be displayed in both block and page preview
		- Unexpected behavior of Ctrl + b
		- Black screen when closing window in fullscreen mode on MacOS
	- [[Enhancement]]
		- Click to edit should jump to the end of inline emphasis and links
		- Smooth transition for left sidebar
		- Make [[DWIM]] optional
			- See more at https://github.com/logseq/logseq/issues/2958#issuecomment-945761631
		- Page suggestion will not allow you to deny the suggestion
		- Enable Enter key to rename page
		- Reload commands when toggle plugins (no need to restart the app)
- [[Oct 12th, 2021]]
  id:: 14cbc67d-695a-48b3-8d33-ddf936977d43
  **Beta 0.4.4**
  Desktop app download link: https://github.com/logseq/logseq/releases/tag/0.4.4
	- [[Fixed issues]]
		- Can't open graph on Linux
		- Performance degradation
		- Favorite when renaming page's title
		- Undo need multiple steps (inserting new block)
		- Recent not working
		- Url can include `{` and `}` now
- [[Oct 11th, 2021]]
  id:: 2c01a84b-d944-4755-bed4-6ff079465567
  **Beta 0.4.3**
  Desktop app download link: https://github.com/logseq/logseq/releases/tag/0.4.3
	- [[Features]]
		- Left sidebar!  🌈  🌈
			-
			  <div style="position: relative; padding-bottom: 93.02325581395348%; height: 0;"><iframe src="https://www.loom.com/embed/5fd05d33377c4254b4ee4b6aae5b193d" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;"></iframe></div>
			-
		- Select multiple blocks to `copy block refs` and `cycle todos`
	- [[Thanks]]
		- [[Ed]]
			- The beautiful https://logseqweekly.com/! Don't forget to subscribe!
				- > With the rapid development of the app and new features/improvements, I created this Weekly Summary to help community members keep up with everything being thought of, created and shared by other fellow Logseq users.
		- [[Mispille]]
			- Awesome proposal to tagging Logseq's issues on GitHub!
				- This proposal is at https://docs.google.com/spreadsheets/d/10-LplNuMo2MUy67lt-WX1z1x50L1pY4bSLPIob1eHRQ/edit?usp=sharing!
		- [[llcc]]
			- [[DWIM]] (do what I mean) for `Enter` key when editing.  
			  Context-awareness of `Enter` key makes editing more easily.
		- [[Devon Zuegel]]
			- Consolidate shortcut docs
		- [[hyrijk]]
			- Fix: plugin api moveBlock not working
		- [[Tomas Vik]]
			- Enhance: pretty print pages-metadata.edn
	- [[Fixed issues]]
		- Data loss when dragging blocks to empty pages
		- Create today's journal when the corresponding file doesn't exist yet
		- Broken block references
			- Remove blank line for some blocks when outputting to md/org
		- Importing from Roam has issues with illegal filenames (Windows)
		- Flashcards wrong number during the review
		- Page rename doesn't work for case-sensitive pages
		- Respect the original page's name in the block content
		- Flashcards don't work when publishing
		- A block can be collapsed only when it has children or its body is not empty
		- Display the edit icon only for the embedded parent block
		- Sanitize html for security (plugins)
		- Disable nested queries (page crash)
		- Support raw path under win32 that includes backslash for local pdf files
		- Goto pdf highlights not working sometimes
		- Markdown footnote definition not working when re-index or refresh
		- preferredThemeMode doesn't work (plugins API)
	- [[Enhancement]]
		- Click title to rename a page
		- Open the first block when opening a new page by Mod+o
		- Many UX enhancements
- [[Changelog_07_09]]
- [[Changelog_06]]
- [[Changelog 2020]]