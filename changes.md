# Calendar.js Change Log:

### Version 0.6.0:
- Added support to remove an event from a repeating series (asked in the confirmation message).
- Holidays (Christmas Eve, Christmas Day, Boxing Day, New Year's Eve and New Year's Day) are now the default holidays.
- Added navigation key support when full-screen mode is activated:
  1. Left:  Moves to the previous month.
  2. Right:  Moves to the next month.
  3. Escape:  Closes full-screen mode.
  4. Down:  Jumps to the current month.
  6. F5:  Refreshes the current view.
  7. Ctrl/Command + F:  Opens the search dialog.
  8. Ctrl/Command + Left:  Moves to the previous year.
  9. Ctrl/Command + Right:  Moves to the next year.
- Added "created" support to events (set automatically if not available to the current date/time).
- Added "organizerName" support to events (set automatically if not available to options > organizerName).
- Added "organizerEmailAddress" support to events (set automatically if not available to options > organizerEmailAddress).
- Added support to export events to the iCAL format.
- Fixed events being in the wrong order when exported (to any format).
- Added public methods "moveToPreviousYear()" and "moveToNextYear()" (with new "on" events).

### Version 0.5.2:
- The text "All Day Event" is now "All-Day" (renamed all the settings to match).
- Fixed a fault that allowed text to be selected in a disabled text field (date, time).
- Added "grid-border-color" that states the border color of the internal grid borders (which is now a lighter gray).
- The day name headers now use 3 letters for the short names by default.
- Added holiday support (shown under day numbers and in the Full Day title bar) as a new option called "holidays".
- Transition effects are no longer shown when the Event Editor is opened (stops things jumping around).
- Fixed a fault that prevented the Search dialog from rebuilding when setting new options.
- Fixed a fault that caused the dialogs to become unresponsive when the main display is rebuilt.
- Fixed a script error occurring when nothing is found in the Search dialog.
- Added include "Title", "Description" and "Location" searching support in the Search dialog.
- Added support to minimize and restore the Search dialog (new button on the toolbar).
- Fixed a fault that caused the Search dialog to redraw every time the search button is pressed on the main toolbar.

### Version 0.5.1:
- Fixed exports (all except CSV) being broken.
- Fixed missing properties on CSV exports.
- Fixed weekly events not showing up in Internet Explorer.

### Version 0.5.0:
- When an API is called that forces a redraw of the main display, all drop-down menus are now hidden.
- Calling the public method "setOptions()" now rebuilds to the main display using the new settings.
- Fixed a fault that caused events to be assigned to the document/window more than once.
- Fixed a fault that prevented the Day drop-down menu from closing when opening the Year Selector drop-down menu.
- The From/To Date/Times on the Event Editor dialog are now joined up (uses less space).
- Fixed a fault that prevented the views from jumping back to the top of the view when opened again.
- Fixed a fault that caused the Full Day date checker loop to keep going (even after finding the event is on that day).
- Fixed an ordering fault in the Weekly View (the days would be ordered in the order they were found, not by date).
- Better responsive sizes for toolbar icons and font-sizes.
- Added event (repeatsEvery) repeating support (every day, week, month, and year), with new text settings.
- Added event (repeatEveryExcludeDays) exclude days for repeating events support (editable via a new dialog).
- Added a new context menu for events (with quick access to Remove and Edit) to all views.
- Fixed a fault that allowed a To time to be smaller than a From time on the Event Editor (for the same day).
- Fixed some of the editing menus items being available when manual editing of events is disabled.
- Decreased the default width of the "Select Colors" dialog.
- Removed the option "fullDayViewEnabled", as it's no longer needed.
- When dragging an event, the target area now shows a highlighted background color.
- When the "maximumEventsPerDayDisplay" value is reached for events, a new label is shown stating how many more exist.
- Added Previous/Next buttons to the toolbar for the Weekly and Day view, allowing you to skip back and forth.
- Fixed a fault that caused events to appear on the wrong that (start of the week was calculated incorrectly).

### Version 0.4.0:
- The Year Selector drop-down now auto-scrolls to the selected year.
- Removed unneeded class variables.
- All title-bar icons now use the "PureCSS" generated images, giving a much cleaner look and feel.
- Fixed a fault that caused optional text fields for Events to show up as "undefined" when edited or exported.
- Added "Location" support to events, with the extra information being shown in full events and tooltips.
- Event tooltip widths now auto-size to the available content (saves a lot of empty space).
- Added support to set the event Color, Text Color and Border Color (color, colorText, colorBorder properties).
- The "Title" field is now the first field in the Event Editor dialog.
- Added a new "..." button next to the Title text box on the event editor (allows choosing the colors for the event).
- Decreased the width of the "Select Export Type" dialog.
- Fixed a fault that allowed bad values through from Times on the Event Editor.
- Fixed a fault that caused bad times (characters other than numbers) to be allowed in events, which never show up.
- Fixed a fault that set the toolbar buttons to the wrong display type.
- The extra toolbar buttons on the main display are now hidden on smaller displays (refresh, export, list all, list week).
- Fixed spelling mistakes across the CSS and JS code for CSS class names.
- Renamed all dialog CSS classes to added "calendar-dialog" CSS class (to allow easier use of custom input styles).
- Added full search support (new "Search" button on the main toolbar), with option to Match Case.
- Fixed the text cursor being shown for text that cannot be selected.ß
- Fixed the Today button redrawing the main display even when the current month is in view.
- Added new option "minimumDayHeight", which allows you to set the height of the days in the main view (defaults to 0 - auto).
- Fixed the check/radio boxes using the full width of the container areas.
- The background color used for the headers on the main display is now a slightly lighter shade of gray.ß
- Weekend days in the main display are now shown in a color as the headers.
- The current day is now indicated by the day number being highlighted (instead of the whole day).
- Building events on the main display is now much faster.
- Updating the toolbar icons on the main display is now based on the events already checked, instead of searching again.
- The element that will hold the Calendar is now cleared before building starts (was causing some strange display issues).
- More JSDoc documentation improvements and type fixes.

### Version 0.3.0:
- Added the custom scrollbar to the textarea on the "Event Editor" dialog.
- The custom scroll-bar now has :hover and :active selectors.
- Added support to use the custom tooltip for every tooltip throughout the views.
- Fixed a fault that prevented the custom tooltips from hiding when the mouse is moved again.
- Fixed a fault that caused the wrong week to be shown when using the calendar on a Sunday.
- Fixed a fault that caused events to not show in the Weekly View when their times are greater than 00:00.
- The Weekly View now shows the From/To dates in the title bar instead of static text (option text removed).
- Fixed the full view content sizes being a few pixels off in height.
- Added transition effects to disabled inputs and check-marks.
- Renamed some of the settings to reflect the default text changes for dates shown on events (starts from, finishes, etc).
- The day name (Monday-Sunday) is now shown on the full day view.
- Fixed a fault that caused the full screen mode to activate when double clicking on buttons and the year selector.
- Added context menu support for days (Add Event, Expand Day).
- Renamed tooltip "View Week Events" to "View Current Week Events".
- Fixed the tooltip text being selectable.
- Fixed some of the dialogs text being selectable.
- Added support to view any week’s events (available in the new day context menu as "View Current Week Events").
- Fixed the Weekly Events view jumping around dates when auto-updating.
- Fixed the current day being highlighted twice (for example, 1st this month, and then 1st in the next month).
- Added support to highlight the current day in the previous month/next month days.
- Fixed a fault that caused the dates to be shown in the wrong format for the Event Editor in Safari and Internet Explorer.
- Invalid dates entered in Safari and Internet Explorer via the Event Editor are now added to today date.
- Auto-update no longer runs when the Year Selector drop-down is visible.
- Fixed the tooltips being shown when a drop-down menu (Years, Context) is visible.
- The Year Selector drop-down menu now highlights the current year.
- Fixed outline issues when focusing on a input/textarea.  They now work in all browsers and have a transition effect.
- Event "id" property values are now maintained when editing or moving the event.
- Fixed an error removing the description from a tooltip when it's not required.
- Safer node adding/removing across the core code.

### Version 0.2.0:
- The from "Date" field is now focused when the Event Editor is opened.
- A confirmation dialog is now shown when removing an event.
- Added "Select Export Type" dialog, with CSV, XML, JSON and TEXT support now available.
- exportAllEvents() now takes a type parameter (accepts csv (default), xml, json and text).
- Added support for full screen mode (double click the main title bar) with optional on/off setting.
- Fixed "click" and "resize" events in the document/window being overridden.
- Fixed a fault that prevented the year drop down menu being cantered correctly.
- The "Expand Day" button is now less intrusive and indicates what it will do.
- Added a styled tooltip for the events in the main display (with new settings).
- Improved SASS support for font-sizes, spacing, cell sizes, and border sizes.
- Auto event updating now only runs when the background of the document body is not displayed.

### Version 0.1.1:
- Added active CSS effects for all clickable elements.
- Minor documentation corrections.

### Version 0.1.0:
- Everything :)