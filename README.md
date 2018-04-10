# emoji-convert-reference
quick lookup reference for converting a unicode emoji. Don't expect much from this - it's basic.

You may have an emoji in unicode from somewhere like https://apps.timwhitlock.info/emoji/tables/unicode, e.g.: U+1F603 (smiling face with open mouth)

## HTML
If you swap out the unicode signifier of your emoji `U+` for a [numberic character reference](https://en.wikipedia.org/wiki/Numeric_character_reference) `&#x` (appending a semi-colon) it's good to go. Unicode is [usually `U+{hex}`](https://en.wikipedia.org/wiki/Unicode#Architecture_and_terminology), but if you just have the decimal reference of the character then we can use a decimal `&#{decimal};` numeric character reference (the unicode one we used previously without the 'x').

E.g.: if your emoji unicode character is `U+1F603`, take the `1F603` hex and place it into a numeric character reference `&#x1F603;`
`<h1>&#x1F603;<h1>`

## Javascript

You can swap out the `U+` with Javascript's hex signifier `0x` and use [String.fromCodePoint()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/fromCodePoint) `U+1F603` -> `0x1F603`.
`console.log(String.fromCodePoint(0x1F603));`

