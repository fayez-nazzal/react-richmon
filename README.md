# Richmon

> Richmon is a new rich text editor for React that is very easy to use and customize, it's currently on the alpha release - new features are listed to be added in future releases.

## Demo
Here's a ['Demo'](https://codesandbox.io/s/flamboyant-hoover-9xtvm?file=/src/App.js) at CodeSandbox.

## Install

```bash
npm install --save richmon
```

## Getting started

```js
import React, { useState } from 'react'

import { Richmon } from 'richmon'

export default () => {
  const [content, setContent] = useState('')

  return (
    <Richmon
      content={content}
      onChange={setContent}
      tools={[
        'BIUS',
        'thin-seperator',
        'sub',
        'sup',
        'thin-seperator',
        'fontSize',
        'textColor',
        'textHighlight',
        'textShadow',
        'thin-seperator',
        'orderedList',
        'unOrderedList',
        'table'
      ]}
    />
  )
}
```

If you don't want a smooth caret, just include the `disableSmoothCaret` prop.

# Customization

Basic customization can be done by providing props to the main `Richmon` Component, check the list of available props below.

If you want to customize more, like providing custom buttons or custom menus there's components like `RichButton`, `RichMenu`, `FontSizeMenu`, `TableMenu` and more, they are listed to be documented soon.

# Props

| Prop                                   | type                               | Required | What it does?                                                                                                                                                |
| -------------------------------------- | ---------------------------------- | -------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| content                                | string                             | true     | Sets initial content for the Editor.                                                                                                                         |
| onChange                               | callback function                  | true     | sets the content for the editor                                                                                                                              |
| tools                                  | array of strings and/or components | true     | sets the ttols in the toolbar like bold, textColor..etc.                                                                                                     |
| width                                  | string                             | false    | the width of the entire component.                                                                                                                           |
| height                                 | string                             | false    | the height of the enire component.                                                                                                                           |
| css                                    | string                             | false    | the css for the entire component (styled components css syntax)                                                                                              |
| editorCss                              | string                             | false    | the css for the Editor (styled components css syntax)                                                                                                        |
| toolbarCss                             | string                             | false    | the css for the Editor (styled components css syntax)                                                                                                        |
| caretColor                             | string                             | false    | sets the color of the caret                                                                                                                                  |
| disableSmoothCaret                     | string                             | false    | disables the smooth caret on the editor, defaults to false.                                                                                                  |
| defaultTextColor                       | string                             | false    | the default text color in the editor.                                                                                                                        |
| defaultFontSize                        | string                             | false    | the default font size in the editor.                                                                                                                         |
| defaultButtonWidth                     | string                             | false    | the default width of buttons in the toolbar.                                                                                                                 |
| defaultHighlightColor                  | string                             | false    | the default highlight color for the text in the editor.                                                                                                      |
| defaultButtonWidth                     | string                             | false    | the default width of buttons in the toolbar.                                                                                                                 |
| defaultButtonHeight                    | string                             | false    | the default height of buttons in the toolbar.                                                                                                                |
| defaultButtonCss                       | string                             | false    | the default css of buttons in the toolbar.                                                                                                                   |
| defaultActionButtonCss                 | string                             | false    | the default css of action buttons in the toolbar, action buttons is in the left of the arrow button in menus like text color menu, text highlight menu..etc. |
| defaultButtonWrapperCss                | string                             | false    | the default css for the button that wraps action button and arrow button on menus.                                                                           |
| caretDelay                             | string                             | false    | the caret transition delay, defaults to '55ms'.                                                                                                              |
| defaultBasicTextColorsRows             | number                             | false    | the number of rows of the basic colors group in text colors menu.                                                                                            |
| defaultBasicTextColorsCols             | number                             | false    | the number of columns of the basic colors group in text colors menu.                                                                                         |
| defaultBasicTextHighlightColorsRows    | number                             | false    | the number of rows of the basic colors group in text highlight menu.                                                                                         |
| defaultBasicTextHighlightColorsCols    | number                             | false    | the number of columns of the basic colors group in text highlight menu.                                                                                      |
| defaultBasicTextShadowColorsRows       | number                             | false    | the number of rows of the basic colors group in text shadow menu.                                                                                            |
| defaultBasicTextShadowColorsCols       | number                             | false    | the number of columns of the basic colors group in text shadow menu.                                                                                         |
| defaultFeaturedTextColorsRows          | number                             | false    | the number of rows of the featured colors group (at the top of the basic colors group) in text colors menu.                                                  |
| defaultFeaturedTextColorsCols          | number                             | false    | the number of columns of the featured colors group (at the top of the basic colors group) in text colors menu.                                               |
| defaultFeaturedTextHighlightColorsRows | number                             | false    | the number of rows of the featured colors group (at the top of the basic colors group) in text highlight number.                                             |
| defaultFeaturedTextHighlightColorsCols | number                             | false    | the number of columns of the featured colors group (at the top of the basic colors group) in text highlight menu.                                            |
| defaultFeaturedTextShadowColorsRows    | number                             | false    | the number of rows of the featured colors group (at the top of the basic colors group) in text shadow menu.                                                  |
| defaultFeaturedTextShadowColorsCols    | number                             | false    | the number of columns of the featured colors group (at the top of the basic colors group) in text shadow menu.                                               |
| defaultCustomTextColorsRows            | number                             | false    | the number of rows of the custom colors group in text colors menu.                                                                                           |
| defaultCustomTextColorsCols            | number                             | false    | the number of columns of the custom colors group in text colors menu.                                                                                        |
| defaultCustomTextHighlightColorsRows   | number                             | false    | the number of rows of the custom colors group in text highlight menu.                                                                                        |
| defaultCustomTextHighlightColorsCols   | number                             | false    | the number of columns of the custom colors group in text highlight menu.                                                                                     |
| defaultCustomTextShadowColorsRows      | number                             | false    | the number of rows of the custom colors group in text shadow menu.                                                                                           |
| defaultCustomTextShadowColorsCols      | number                             | false    | the number of columns of the custom colors group in text shadow menu.                                                                                        |
| textColorsHasCustom                    | boolean                            | false    | sets if the text colors menu has custom colors group.                                                                                                        |
| textHighlightColorsHasCustom           | boolean                            | false    | sets if the text highlight menu has custom colors group.                                                                                                     |
| textShadowColorsHasCustom              | boolean                            | false    | sets if the text shadow menu has custom colors group.                                                                                                        |
| defaultBasicTextColorsCss              | string                             | false    | sets the css of the basic color palletes in the text color menu.                                                                                             |
| defaultFeaturedTextColorsCss           | array of strings                   | false    | sets the css of the featured color palletes in the text color menu.                                                                                          |
| defaultBasicTextHighlightColorsCss     | array of strings                   | false    | sets the css of the featured color palletes in the text highlight menu.                                                                                      |
| defaultBasicTextShadowColorsCss        | array of strings                   | false    | sets the css of the basic color palletes in the text shadow menu.                                                                                            |
| defaultFeaturedTextShadowColorsCss     | array of strings                   | false    | sets the css of the featured color palletes in the text shadow menu.                                                                                         |
| defaultBasicTextHighlightColorsCss     | array of strings                   | false    | sets the css of the basic color palletes in the text highlight menu.                                                                                         |
| defaultFeaturedTextHighlightColors     | array of strings                   | false    | sets the css of the featured color palletes in the text highlight menu.                                                                                      |
| defaultBasicTextColors                 | array of strings                   | false    | sets the basic color pallets for the text color menu (hex, rgb..etc).                                                                                        |
| defaultFeaturedTextColors              | array of strings                   | false    | sets the featured color pallets for the text color menu (hex, rgb..etc).                                                                                     |
| defaultBasicTextHighlightColors        | array of strings                   | false    | sets the basic color pallets for the text highlight menu (hex, rgb..etc).                                                                                    |
| defaultFeaturedTextHighlightColors     | array of strings                   | false    | sets the featured color pallets for the text highlight menu (hex, rgb..etc).                                                                                 |
| defaultBasicTextShadowColors           | array of strings                   | false    | sets the basic color pallets for the text shadow menu (hex, rgb..etc).                                                                                       |
| defaultFeaturedTextShadowColors        | array of strings                   | false    | sets the featured color pallets for the text shadow menu (hex, rgb..etc).                                                                                    |

# Todos

- add image and file upload support
- write full documentation
- provide inline tools for tables and images

For suggestions just open an issue.

## License

MIT © [fayez-nazzal](https://github.com/fayez-nazzal)

<div>List icons made by <a href="https://www.flaticon.com/authors/dave-gandy" title="Dave Gandy">Dave Gandy</a> from <a href="https://www.flaticon.com/" title="Flaticon">www.flaticon.com</a></div>
