# ScripTless lite

A command line tool to navigate and scan webapplications.

## Run instruction
Install JDK8: https://www.oracle.com/in/java/technologies/javase/javase8-archive-downloads.html
Install 7zipk: https://www.7-zip.org/download.html
Dowload chromedriver or msedgedriver according to the browser version

Download all scriptless-cli split zip files and merge split zip files with 7zip
Download config.prop and keep at same folder as the scriptless-cli jar.
Updated the config.prop for driver type and location

Run:
java -Xmx1024m -Xms1024m -jar scriptless-cli-[version].RELEASE.jar

## Features
- **Clears data**
  - Clears either all data, objects, or actions based on the provided option.

- **Reads Action details from a file**
  - Reads action details from a CSV file specified by the path.
  - Reports the number of actions loaded successfully.

- **Print path to the (working) directory where the Actions and Objects are being stored**
  - Prints the path to the working directory where actions and objects are stored.

- **Will kill the webdriver and exit this application**
  - Exits the application after killing the webdriver and necessary processes.

- **Edit files**
  - Allows editing files (actions or objects) based on the provided type (action or object).
  - Opens the file in a text editor for editing.
  - Updates the actions or objects after editing.

- **Shows last data load time**
  - Displays the last time when object and action data were updated.

- **Reads Object details from files**
  - Reads object details from files based on the specified format (CSV, JSON-key-value, LOC).
  - Allows selecting the format interactively if not provided.

- **Show Action Details**
  - Displays action details based on specified screens or all screens.
  - Filters actions based on provided screens.

- **Move to screen**
  - Moves to a specific screen from another screen.

- **Switch window**
  - Switches between windows based on the provided action (search, move by handle, move by title, print current window).

- **Run any scriptless command**
  - Executes a scriptless command like loading a URL or other actions specified by the action parameter.

- **Switch frame**
  - Switches between frames on a web page.

- **Scans a specific Screen**
  - Scans a specific screen for objects and actions.

- **Highlight element(s) on current screen by xpath**
  - Highlights elements on the current screen based on provided xpath.

- **Highlight element(s) on current screen by condition**
  - Highlights elements on the current screen based on provided condition.

- **Move to a Screen from the beginning**
  - Moves to a specific screen from the beginning.

- **Scans current Screen**
  - Scans the current screen for objects based on provided types.

- **Validate objects**
  - Validates objects based on provided parameters.

- **Start a browser with a URL**
  - Starts a browser and navigates to the provided URL.

- **Reload properties from config.prop**
  - Reloads properties from the configuration file.

- **Show Object Details**
  - Displays object details based on specified screens or all screens.

- **Export Action data**
  - Exports action data to a file specified by the path.

- **Export Object data**
  - Exports object data to a file specified by the path and format.

- **Export Object alt. Xpaths data**
  - Exports alternative XPaths of objects to a file specified by the path.

- **Shows memory details**
  - Displays details about memory usage.


## AVAILABLE COMMANDS

### data
- **ed, edit**: Edit files.
- **expact, xa**: Export Action data.
- **expobj, xo**: Export Object data.
- **la, loadact**: Reads Action details from a file.
- **ldt**: Shows last data load time.
- **lo, loadobject**: Reads Object details from files.
- **sa, showaction**: Show Action Details.
- **showobj, so**: Show Object Details.

### scan
- **moveto, mt**: Move to a Screen from the beginning.
- **movetopart, mtp**: Move to screen.
- **sc, scan**: Scans a specific Screen.
- **scancur, scr**: Scans current Screen.
- **sf, switchframe**: Switch frame.
- **start**: Start a browser with a URL.
- **sw, switchwindow**: Switch window.
- **validate, vo**: Validate objects.
- **xov**: Export Object alt. Xpaths data.

### util
- **clr**: Clears data.
- **cmd**: Run any scriptless command. Example: `cmd loadurl <url>`.
- **health**: Shows memory details.
- **hello**: Highlight element(s) on current screen by condition.
- **hi**: Highlight element(s) on current screen by XPath.
- **pwd**: Print path to the (working) directory where the Actions and Objects are being stored.
- **reset**: Reload properties from `config.prop`.
- **stop**: Will kill the WebDriver and exit this application.

### Built-In Commands
- **clear**: Clear the shell screen.
- **help**: Display help about available commands.
- **history**: Display or save the history of previously run commands.
- **script**: Read and execute commands from a file.
- **stacktrace**: Display the full stacktrace of the last error.


## List of Possible Actions
1. **clickbutton**: Click a button identified by its XPath.
2. **clicklink**: Click a link identified by its XPath.
3. **selectoption**: Select an option in a dropdown by its XPath and value.
4. **selectoptionall**: Select all options in a dropdown by their XPath and value.
5. **selectoptionbyindex**: Select an option in a dropdown by its XPath and index.
6. **selectoptionbyvalue**: Select an option in a dropdown by its XPath and value.
7. **selectoptionbytext**: Select an option in a dropdown by its XPath and visible text.
8. **deselectoptionall**: Deselect all options in a dropdown by their XPath and value.
9. **deselectoptionbyindex**: Deselect an option in a dropdown by its XPath and index.
10. **deselectoptionbyvalue**: Deselect an option in a dropdown by its XPath and value.
11. **deselectoptionbytext**: Deselect an option in a dropdown by its XPath and visible text.
12. **selectradio**: Select a radio button by its XPath and value.
13. **selectradiobyindex**: Select a radio button by its XPath and index.
14. **selectradiobyvalue**: Select a radio button by its XPath and value.
15. **selectcheckbox**: Select a checkbox by its XPath and value.
16. **selectcheckboxall**: Select all checkboxes by their XPath and value.
17. **selectcheckboxbyindex**: Select a checkbox by its XPath and index.
18. **selectcheckboxbyvalue**: Select a checkbox by its XPath and value.
19. **deselectcheckbox**: Deselect a checkbox by its XPath and value.
20. **deselectcheckboxall**: Deselect all checkboxes by their XPath and value.
21. **deselectcheckboxbyindex**: Deselect a checkbox by its XPath and index.
22. **deselectcheckboxbyvalue**: Deselect a checkbox by its XPath and value.
23. **submit**: Submit a form identified by its XPath.
24. **inputtxt**: Input text into a text field identified by its XPath.
25. **delay_time**: Delay execution for a specified duration.
26. **delay_till_clickable**: Delay until an object is clickable.
27. **delay_till_visible**: Delay until an object is visible.
28. **loadurl**: Load a URL in the browser.
29. **NotVisibleAtXPATH**: Assert that an element is not visible at the specified XPath.
30. **VisibleAtXPATH**: Assert that an element is visible at the specified XPath.
31. **AssertBetween**: Assert that a value is between a range.
32. **AssertNotBetween**: Assert that a value is not between a range.
33. **AssertEqual**: Assert that a value is equal to the expected value.
34. **AssertNotEqual**: Assert that a value is not equal to the expected value.
35. **AssertEqualFormat**: Assert that a value matches a specific format.
36. **AssertNotEqualFormat**: Assert that a value does not match a specific format.
37. **AssertGreater**: Assert that a value is greater than the expected value.
38. **AssertGreaterEqual**: Assert that a value is greater than or equal to the expected value.
39. **AssertLess**: Assert that a value is less than the expected value.
40. **AssertLessEqual**: Assert that a value is less than or equal to the expected value.
41. **AssertInList**: Assert that a value is in a list of expected values.
42. **AssertNotInList**: Assert that a value is not in a list of expected values.
43. **AssertIsNotNumber**: Assert that a value is not a number.
44. **AssertIsNumber**: Assert that a value is a number.
45. **AssertNotLess**: Assert that a value is not less than the expected value.
46. **AssertNotGreater**: Assert that a value is not greater than the expected value.
47. **switch-frame**: Switch to a specified frame by its name or ID.
48. **switch-frame-parent**: Switch to the parent frame.
49. **switch-frame-context**: Switch to a frame by context.
50. **fetch-current-frame**: Fetch the current frame.
51. **switch-window-handle**: Switch to a window by its handle.
52. **switch-window-title**: Switch to a window by its title.
53. **mouse-hover**: Hover the mouse over an element identified by its XPath.
54. **mouse-click**: Click on an element using the mouse identified by its XPath.
55. **mouse-double-click**: Double-click on an element using the mouse identified by its XPath.
56. **close-window**: Close the current window.
57. **alert-accept**: Accept an alert.
58. **alert-dismiss**: Dismiss an alert.
59. **alert-assert-equal**: Assert that the alert text is equal to the expected text.
60. **alert-assert-notequal**: Assert that the alert text is not equal to the expected text.
