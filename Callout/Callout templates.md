<%*
selection = tp.file.selection()
const callouts = {
	'grid|col-2': ' ƒ  grid (2 column in default, option: 3, 4)',
	'grid|25%': ' ƒ  two non-even column grid (25% column in default, option: 33%, 75%)',
	Note: '🟦 Note',
	Info: '🟦 Info',
	Todo: '🟦 Todo',
	Summary: '💧 Summary/Abstract',
	Tip: '💧 Tip/Hint/Important',
	Check: '🟩 Success, Check, Done',
	FAQ: '🟧 Question, Help, FAQ',
	Caution: '🟧 Warning, Caution, Attention',
	Fail: '🟥 Failure, Fail, Missing',
	Error: '🟥 Danger, Error',
	Bug: '🟥 Bug',
	Example: '🟪 Example',
	Cite: '⬛ Quote, Cite'
}
// return callout
const type = await tp.system.suggester(Object.values(callouts), Object.keys(callouts), true, 'Select callout type.');
return "> [!"+type+"]\n>"
-%>