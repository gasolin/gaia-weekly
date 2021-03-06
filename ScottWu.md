## 12/27 ~ 12/30

- [Firefox]
	- [UI feedback] [Bug 285836](https://bugzilla.mozilla.org/show_bug.cgi?id=285836) - Make "Remove All Cookies Now" undoable
		- Got UX feedback, will make a few changes to the patch

- [Date-time Picker]
	- [Bug 1283381](https://bugzilla.mozilla.org/show_bug.cgi?id=1283381) - [meta] Implement UI for date time input types
		- [Bug 1320225](https://bugzilla.mozilla.org/show_bug.cgi?id=1320225) - [DateTimeInput] Integration of input type=date input box with picker
			- Ready for review, waiting for :mconley to get back from holidays
		- [Bug 1320647](https://bugzilla.mozilla.org/show_bug.cgi?id=1320647) -  [DateTimePicker] Add min/max and step support to date picker
			- Added step support for month & year
			- Will request for review after Bug 1320225 and Bug 1325922 land
		- [Bug 1325922](https://bugzilla.mozilla.org/show_bug.cgi?id=1325922) - [DateTimePicker] Add arrows svg file and style month-year button for date picker
			- Ready for review
- [Form Autofill]
	-  [Bug 1304306](https://bugzilla.mozilla.org/show_bug.cgi?id=1304306) - Need to have a place in the Preference -> Setting for users to launch the profile list add/edit/remove dialog
		-  WIP on mozreview
		-  Asking :MattN for his feedback
	-  [Bug 1326153](https://bugzilla.mozilla.org/show_bug.cgi?id=1326153) - [Form Autofill] Change the feature flag to browser.formautofill.experimental
		-  Patch on mozreview
		-  Addressing question from :MattN

#### Date Time Pickers Tasks:

- General features
	- [Done] Passing data between input field and pickers
	- [Hold] Keyboard Controls
		- To be implemented in follow up bugs
		- Input box handles keyboard events most of the time, until user triggers shifting "visual focus" to picker
- Month picker
	- [Done] Spinner component (basic functionalities)
	- [Hold] Spinners are combined when indivisible step is used
		- UX considering removing this from the spec
- Time picker
	- [Done] AM/PM component
	- [Done] Spinner cycle feature
	- [Done] Spinner scroll snap even with few items
	- [Done] Extract time state handling into a module
	- [Done] Changed how updates are handled to make sure it works for years
	- [Done] Integrate with input boxes
	- [Done] Out of range items are displayed but greyed out
	- [Done] Fix panel arrow position
- Date picker
	- [Done] Basic calendar component
		- Display calendar in 6 week rows
		- First day of the week & weekends configurable
		- Apply basic styling
	- [Done] Add max and min features
		- Dates earlier than min or later than max are greyed out
		- Out of range years are not displayed, and months are greyed out
	- Add step features
		- Off step items are greyed out
	- Transition animation
		- Animation for previous and next month
		- Animation for opening picker
- Week picker
	- Calendar week feature
- Datetime picker
	- Combining date picker and time picker

- Full L10n support
	- Getting localized strings with Intl API
	- Get calendar info with Intl API
	- Spinner orders depend on locale
- Full a11y support
	- Tab focus
	- Alt text & ARIA
