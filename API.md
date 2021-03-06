<!-- Generated by documentation.js. Update this documentation by updating the source code. -->

### Table of Contents

-   [assert.dom()][1]
-   [DOMAssertions][2]
    -   [exists][3]
        -   [Parameters][4]
        -   [Examples][5]
    -   [doesNotExist][6]
        -   [Parameters][7]
        -   [Examples][8]
    -   [isChecked][9]
        -   [Parameters][10]
        -   [Examples][11]
    -   [isNotChecked][12]
        -   [Parameters][13]
        -   [Examples][14]
    -   [isFocused][15]
        -   [Parameters][16]
        -   [Examples][17]
    -   [isNotFocused][18]
        -   [Parameters][19]
        -   [Examples][20]
    -   [isRequired][21]
        -   [Parameters][22]
        -   [Examples][23]
    -   [isNotRequired][24]
        -   [Parameters][25]
        -   [Examples][26]
    -   [isValid][27]
        -   [Parameters][28]
        -   [Examples][29]
    -   [isVisible][30]
        -   [Parameters][31]
        -   [Examples][32]
    -   [isNotVisible][33]
        -   [Parameters][34]
        -   [Examples][35]
    -   [hasAttribute][36]
        -   [Parameters][37]
        -   [Examples][38]
    -   [doesNotHaveAttribute][39]
        -   [Parameters][40]
        -   [Examples][41]
    -   [hasAria][42]
        -   [Parameters][43]
        -   [Examples][44]
    -   [doesNotHaveAria][45]
        -   [Parameters][46]
        -   [Examples][47]
    -   [hasProperty][48]
        -   [Parameters][49]
        -   [Examples][50]
    -   [isDisabled][51]
        -   [Parameters][52]
        -   [Examples][53]
    -   [isNotDisabled][54]
        -   [Parameters][55]
        -   [Examples][56]
    -   [hasClass][57]
        -   [Parameters][58]
        -   [Examples][59]
    -   [doesNotHaveClass][60]
        -   [Parameters][61]
        -   [Examples][62]
    -   [hasStyle][63]
        -   [Parameters][64]
        -   [Examples][65]
    -   [hasPseudoElementStyle][66]
        -   [Parameters][67]
        -   [Examples][68]
    -   [doesNotHaveStyle][69]
        -   [Parameters][70]
        -   [Examples][71]
    -   [doesNotHavePseudoElementStyle][72]
        -   [Parameters][73]
        -   [Examples][74]
    -   [hasText][75]
        -   [Parameters][76]
        -   [Examples][77]
    -   [hasAnyText][78]
        -   [Parameters][79]
        -   [Examples][80]
    -   [hasNoText][81]
        -   [Parameters][82]
        -   [Examples][83]
    -   [includesText][84]
        -   [Parameters][85]
        -   [Examples][86]
    -   [doesNotIncludeText][87]
        -   [Parameters][88]
        -   [Examples][89]
    -   [hasValue][90]
        -   [Parameters][91]
        -   [Examples][92]
    -   [hasAnyValue][93]
        -   [Parameters][94]
        -   [Examples][95]
    -   [hasNoValue][96]
        -   [Parameters][97]
        -   [Examples][98]
    -   [matchesSelector][99]
        -   [Parameters][100]
        -   [Examples][101]
    -   [doesNotMatchSelector][102]
        -   [Parameters][103]
        -   [Examples][104]
    -   [hasTagName][105]
        -   [Parameters][106]
        -   [Examples][107]
    -   [doesNotHaveTagName][108]
        -   [Parameters][109]
        -   [Examples][110]

## assert.dom()

Once installed the DOM element assertions are available at `assert.dom(...).*`:

**Parameters**

-   `target` **([string][111] \| [HTMLElement][112])** A CSS selector that can be used to find elements using [`querySelector()`][113], or an [HTMLElement][] (Not all assertions support both target types.) (optional, default `rootElement` or `document`)
-   `rootElement` **[HTMLElement][112]?** The root element of the DOM in which to search for the `target` (optional, default `document`)

**Examples**

```javascript
test('the title exists', function(assert) {
  assert.dom('#title').exists();
});
```


## DOMAssertions

### exists

-   **See: [#doesNotExist][114]
    **

Assert an [HTMLElement][115] (or multiple) matching the `selector` exists.

#### Parameters

-   `options` **[object][116]?** 
    -   `options.count` **[number][117]?** 
-   `message` **[string][118]?** 

#### Examples

```javascript
assert.dom('#title').exists();
assert.dom('.choice').exists({ count: 4 });
```

### doesNotExist

-   **See: [#exists][3]
    **

Assert an [HTMLElement][115] matching the `selector` does not exists.

#### Parameters

-   `message` **[string][118]?** 

#### Examples

```javascript
assert.dom('.should-not-exist').doesNotExist();
```

### isChecked

-   **See: [#isNotChecked][119]
    **

Assert that the [HTMLElement][115] or an [HTMLElement][115] matching the
`selector` is currently checked.

Note: This also supports `aria-checked="true/false"`.

#### Parameters

-   `message` **[string][118]?** 

#### Examples

```javascript
assert.dom('input.active').isChecked();
```

### isNotChecked

-   **See: [#isChecked][120]
    **

Assert that the [HTMLElement][115] or an [HTMLElement][115] matching the
`selector` is currently unchecked.

Note: This also supports `aria-checked="true/false"`.

#### Parameters

-   `message` **[string][118]?** 

#### Examples

```javascript
assert.dom('input.active').isNotChecked();
```

### isFocused

-   **See: [#isNotFocused][121]
    **

Assert that the [HTMLElement][115] or an [HTMLElement][115] matching the
`selector` is currently focused.

#### Parameters

-   `message` **[string][118]?** 

#### Examples

```javascript
assert.dom('input.email').isFocused();
```

### isNotFocused

-   **See: [#isFocused][122]
    **

Assert that the [HTMLElement][115] or an [HTMLElement][115] matching the
`selector` is not currently focused.

#### Parameters

-   `message` **[string][118]?** 

#### Examples

```javascript
assert.dom('input[type="password"]').isNotFocused();
```

### isRequired

-   **See: [#isNotRequired][123]
    **

Assert that the [HTMLElement][115] or an [HTMLElement][115] matching the
`selector` is currently required.

#### Parameters

-   `message` **[string][118]?** 

#### Examples

```javascript
assert.dom('input[type="text"]').isRequired();
```

### isNotRequired

-   **See: [#isRequired][124]
    **

Assert that the [HTMLElement][115] or an [HTMLElement][115] matching the
`selector` is currently not required.

#### Parameters

-   `message` **[string][118]?** 

#### Examples

```javascript
assert.dom('input[type="text"]').isNotRequired();
```

### isValid

-   **See: [#isValid][125]
    **

Assert that the [HTMLElement][115] passes validation

Validity is determined by asserting that:

-   `element.reportValidity() === true`

#### Parameters

-   `message` **[string][118]?** 

#### Examples

```javascript
assert.dom('.input').isValid();
```

### isVisible

-   **See: [#isNotVisible][126]
    **

Assert that the [HTMLElement][115] or an [HTMLElement][115] matching the
`selector` exists and is visible.

Visibility is determined by asserting that:

-   the element's offsetWidth and offsetHeight are non-zero
-   any of the element's DOMRect objects have a non-zero size

Additionally, visibility in this case means that the element is visible on the page,
but not necessarily in the viewport.

#### Parameters

-   `options` **[object][116]?** 
    -   `options.count` **[number][117]?** 
-   `message` **[string][118]?** 

#### Examples

```javascript
assert.dom('#title').isVisible();
assert.dom('.choice').isVisible({ count: 4 });
```

### isNotVisible

-   **See: [#isVisible][127]
    **

Assert that the [HTMLElement][115] or an [HTMLElement][115] matching the
`selector` does not exist or is not visible on the page.

Visibility is determined by asserting that:

-   the element's offsetWidth or offsetHeight are zero
-   all of the element's DOMRect objects have a size of zero

Additionally, visibility in this case means that the element is visible on the page,
but not necessarily in the viewport.

#### Parameters

-   `message` **[string][118]?** 

#### Examples

```javascript
assert.dom('.foo').isNotVisible();
```

### hasAttribute

-   **See: [#doesNotHaveAttribute][128]
    **

Assert that the [HTMLElement][115] has an attribute with the provided `name`
and optionally checks if the attribute `value` matches the provided text
or regular expression.

#### Parameters

-   `name` **[string][118]** 
-   `value` **([string][118] \| [RegExp][129] \| [object][116]?)** 
-   `message` **[string][118]?** 

#### Examples

```javascript
assert.dom('input.password-input').hasAttribute('type', 'password');
```

### doesNotHaveAttribute

-   **See: [#hasAttribute][130]
    **

Assert that the [HTMLElement][115] has no attribute with the provided `name`.

**Aliases:** `hasNoAttribute`, `lacksAttribute`

#### Parameters

-   `name` **[string][118]** 
-   `message` **[string][118]?** 

#### Examples

```javascript
assert.dom('input.username').hasNoAttribute('disabled');
```

### hasAria

-   **See: [#hasNoAria][131]
    **

Assert that the [HTMLElement][115] has an ARIA attribute with the provided
`name` and optionally checks if the attribute `value` matches the provided
text or regular expression.

#### Parameters

-   `name` **[string][118]** 
-   `value` **([string][118] \| [RegExp][129] \| [object][116]?)** 
-   `message` **[string][118]?** 

#### Examples

```javascript
assert.dom('button').hasAria('pressed', 'true');
```

### doesNotHaveAria

-   **See: [#hasAria][132]
    **

Assert that the [HTMLElement][115] has no ARIA attribute with the
provided `name`.

#### Parameters

-   `name` **[string][118]** 
-   `message` **[string][118]?** 

#### Examples

```javascript
assert.dom('button').doesNotHaveAria('pressed');
```

### hasProperty

-   **See: [#doesNotHaveProperty][133]
    **

Assert that the [HTMLElement][115] has a property with the provided `name`
and checks if the property `value` matches the provided text or regular
expression.

#### Parameters

-   `name` **[string][118]** 
-   `value` **([string][118] \| [RegExp][129])** 
-   `message` **[string][118]?** 

#### Examples

```javascript
assert.dom('input.password-input').hasProperty('type', 'password');
```

### isDisabled

-   **See: [#isNotDisabled][134]
    **

Assert that the [HTMLElement][115] or an [HTMLElement][115] matching the
`selector` is disabled.

#### Parameters

-   `message` **[string][118]?** 

#### Examples

```javascript
assert.dom('.foo').isDisabled();
```

### isNotDisabled

-   **See: [#isDisabled][135]
    **

Assert that the [HTMLElement][115] or an [HTMLElement][115] matching the
`selector` is not disabled.

**Aliases:** `isEnabled`

#### Parameters

-   `message` **[string][118]?** 

#### Examples

```javascript
assert.dom('.foo').isNotDisabled();
```

### hasClass

-   **See: [#doesNotHaveClass][136]
    **

Assert that the [HTMLElement][115] has the `expected` CSS class using
[`classList`][137].

`expected` can also be a regular expression, and the assertion will return
true if any of the element's CSS classes match.

#### Parameters

-   `expected` **([string][118] \| [RegExp][129])** 
-   `message` **[string][118]?** 

#### Examples

```javascript
assert.dom('input[type="password"]').hasClass('secret-password-input');
```

```javascript
assert.dom('input[type="password"]').hasClass(/.*password-input/);
```

### doesNotHaveClass

-   **See: [#hasClass][138]
    **

Assert that the [HTMLElement][115] does not have the `expected` CSS class using
[`classList`][137].

`expected` can also be a regular expression, and the assertion will return
true if none of the element's CSS classes match.

**Aliases:** `hasNoClass`, `lacksClass`

#### Parameters

-   `expected` **([string][118] \| [RegExp][129])** 
-   `message` **[string][118]?** 

#### Examples

```javascript
assert.dom('input[type="password"]').doesNotHaveClass('username-input');
```

```javascript
assert.dom('input[type="password"]').doesNotHaveClass(/username-.*-input/);
```

### hasStyle

-   **See: [#hasClass][138]
    **

Assert that the [HTMLElement][] has the `expected` style declarations using
[`window.getComputedStyle`][139].

#### Parameters

-   `expected` **[object][116]** 
-   `message` **[string][118]?** 

#### Examples

```javascript
assert.dom('.progress-bar').hasStyle({
  opacity: 1,
  display: 'block'
});
```

### hasPseudoElementStyle

-   **See: [#hasClass][138]
    **

Assert that the pseudo element for `selector` of the [HTMLElement][] has the `expected` style declarations using
[`window.getComputedStyle`][139].

#### Parameters

-   `selector` **[string][118]** 
-   `expected` **[object][116]** 
-   `message` **[string][118]?** 

#### Examples

```javascript
assert.dom('.progress-bar').hasPseudoElementStyle(':after', {
  content: '";"',
});
```

### doesNotHaveStyle

-   **See: [#hasClass][138]
    **

Assert that the [HTMLElement][] does not have the `expected` style declarations using
[`window.getComputedStyle`][139].

#### Parameters

-   `expected` **[object][116]** 
-   `message` **[string][118]?** 

#### Examples

```javascript
assert.dom('.progress-bar').doesNotHaveStyle({
  opacity: 1,
  display: 'block'
});
```

### doesNotHavePseudoElementStyle

-   **See: [#hasClass][138]
    **

Assert that the pseudo element for `selector` of the [HTMLElement][] does not have the `expected` style declarations using
[`window.getComputedStyle`][139].

#### Parameters

-   `selector` **[string][118]** 
-   `expected` **[object][116]** 
-   `message` **[string][118]?** 

#### Examples

```javascript
assert.dom('.progress-bar').doesNotHavePseudoElementStyle(':after', {
  content: '";"',
});
```

### hasText

-   **See: [#includesText][140]
    **

Assert that the text of the [HTMLElement][115] or an [HTMLElement][115]
matching the `selector` matches the `expected` text, using the
[`textContent`][141]
attribute and stripping/collapsing whitespace.

`expected` can also be a regular expression.

> Note: This assertion will collapse whitespace if the type you pass in is a string.
> If you are testing specifically for whitespace integrity, pass your expected text
> in as a RegEx pattern.

**Aliases:** `matchesText`

#### Parameters

-   `expected` **([string][118] \| [RegExp][129])** 
-   `message` **[string][118]?** 

#### Examples

```javascript
// <h2 id="title">
//   Welcome to <b>QUnit</b>
// </h2>

assert.dom('#title').hasText('Welcome to QUnit');
```

```javascript
assert.dom('.foo').hasText(/[12]\d{3}/);
```

### hasAnyText

-   **See: [#hasText][142]
    **

Assert that the `textContent` property of an [HTMLElement][115] is not empty.

#### Parameters

-   `message` **[string][118]?** 

#### Examples

```javascript
assert.dom('button.share').hasAnyText();
```

### hasNoText

-   **See: [#hasNoText][143]
    **

Assert that the `textContent` property of an [HTMLElement][115] is empty.

#### Parameters

-   `message` **[string][118]?** 

#### Examples

```javascript
assert.dom('div').hasNoText();
```

### includesText

-   **See: [#hasText][142]
    **

Assert that the text of the [HTMLElement][115] or an [HTMLElement][115]
matching the `selector` contains the given `text`, using the
[`textContent`][141]
attribute.

> Note: This assertion will collapse whitespace in `textContent` before searching.
> If you would like to assert on a string that _should_ contain line breaks, tabs,
> more than one space in a row, or starting/ending whitespace, use the [#hasText][142]
> selector and pass your expected text in as a RegEx pattern.

**Aliases:** `containsText`, `hasTextContaining`

#### Parameters

-   `text` **[string][118]** 
-   `message` **[string][118]?** 

#### Examples

```javascript
assert.dom('#title').includesText('Welcome');
```

### doesNotIncludeText

Assert that the text of the [HTMLElement][115] or an [HTMLElement][115]
matching the `selector` does not include the given `text`, using the
[`textContent`][141]
attribute.

**Aliases:** `doesNotContainText`, `doesNotHaveTextContaining`

#### Parameters

-   `text` **[string][118]** 
-   `message` **[string][118]?** 

#### Examples

```javascript
assert.dom('#title').doesNotIncludeText('Welcome');
```

### hasValue

-   **See: [#hasAnyValue][144]
    **
-   **See: [#hasNoValue][145]
    **

Assert that the `value` property of an [HTMLInputElement][146] matches
the `expected` text or regular expression.

If no `expected` value is provided, the assertion will fail if the
`value` is an empty string.

#### Parameters

-   `expected` **([string][118] \| [RegExp][129] \| [object][116]?)** 
-   `message` **[string][118]?** 

#### Examples

```javascript
assert.dom('input.username').hasValue('HSimpson');
```

### hasAnyValue

-   **See: [#hasValue][147]
    **
-   **See: [#hasNoValue][145]
    **

Assert that the `value` property of an [HTMLInputElement][146] is not empty.

#### Parameters

-   `message` **[string][118]?** 

#### Examples

```javascript
assert.dom('input.username').hasAnyValue();
```

### hasNoValue

-   **See: [#hasValue][147]
    **
-   **See: [#hasAnyValue][144]
    **

Assert that the `value` property of an [HTMLInputElement][146] is empty.

**Aliases:** `lacksValue`

#### Parameters

-   `message` **[string][118]?** 

#### Examples

```javascript
assert.dom('input.username').hasNoValue();
```

### matchesSelector

Assert that the target selector selects only Elements that are also selected by
compareSelector.

#### Parameters

-   `compareSelector` **[string][118]** 
-   `message` **[string][118]?** 

#### Examples

```javascript
assert.dom('p.red').matchesSelector('div.wrapper p:last-child')
```

### doesNotMatchSelector

Assert that the target selector selects only Elements that are not also selected by
compareSelector.

#### Parameters

-   `compareSelector` **[string][118]** 
-   `message` **[string][118]?** 

#### Examples

```javascript
assert.dom('input').doesNotMatchSelector('input[disabled]')
```

### hasTagName

Assert that the tagName of the [HTMLElement][115] or an [HTMLElement][115]
matching the `selector` matches the `expected` tagName, using the
[`tagName`][148]
property of the [HTMLElement][115].

#### Parameters

-   `tagName`  
-   `message` **[string][118]?** 
-   `expected` **[string][118]** 

#### Examples

```javascript
// <h1 id="title">
//   Title
// </h1>

assert.dom('#title').hasTagName('h1');
```

### doesNotHaveTagName

Assert that the tagName of the [HTMLElement][115] or an [HTMLElement][115]
matching the `selector` does not match the `expected` tagName, using the
[`tagName`][148]
property of the [HTMLElement][115].

#### Parameters

-   `tagName`  
-   `message` **[string][118]?** 
-   `expected` **[string][118]** 

#### Examples

```javascript
// <section id="block">
//   Title
// </section>

assert.dom('section#block').doesNotHaveTagName('div');
```

[1]: #assertdom

[2]: #domassertions

[3]: #exists

[4]: #parameters

[5]: #examples

[6]: #doesnotexist

[7]: #parameters-1

[8]: #examples-1

[9]: #ischecked

[10]: #parameters-2

[11]: #examples-2

[12]: #isnotchecked

[13]: #parameters-3

[14]: #examples-3

[15]: #isfocused

[16]: #parameters-4

[17]: #examples-4

[18]: #isnotfocused

[19]: #parameters-5

[20]: #examples-5

[21]: #isrequired

[22]: #parameters-6

[23]: #examples-6

[24]: #isnotrequired

[25]: #parameters-7

[26]: #examples-7

[27]: #isvalid

[28]: #parameters-8

[29]: #examples-8

[30]: #isvisible

[31]: #parameters-9

[32]: #examples-9

[33]: #isnotvisible

[34]: #parameters-10

[35]: #examples-10

[36]: #hasattribute

[37]: #parameters-11

[38]: #examples-11

[39]: #doesnothaveattribute

[40]: #parameters-12

[41]: #examples-12

[42]: #hasaria

[43]: #parameters-13

[44]: #examples-13

[45]: #doesnothavearia

[46]: #parameters-14

[47]: #examples-14

[48]: #hasproperty

[49]: #parameters-15

[50]: #examples-15

[51]: #isdisabled

[52]: #parameters-16

[53]: #examples-16

[54]: #isnotdisabled

[55]: #parameters-17

[56]: #examples-17

[57]: #hasclass

[58]: #parameters-18

[59]: #examples-18

[60]: #doesnothaveclass

[61]: #parameters-19

[62]: #examples-19

[63]: #hasstyle

[64]: #parameters-20

[65]: #examples-20

[66]: #haspseudoelementstyle

[67]: #parameters-21

[68]: #examples-21

[69]: #doesnothavestyle

[70]: #parameters-22

[71]: #examples-22

[72]: #doesnothavepseudoelementstyle

[73]: #parameters-23

[74]: #examples-23

[75]: #hastext

[76]: #parameters-24

[77]: #examples-24

[78]: #hasanytext

[79]: #parameters-25

[80]: #examples-25

[81]: #hasnotext

[82]: #parameters-26

[83]: #examples-26

[84]: #includestext

[85]: #parameters-27

[86]: #examples-27

[87]: #doesnotincludetext

[88]: #parameters-28

[89]: #examples-28

[90]: #hasvalue

[91]: #parameters-29

[92]: #examples-29

[93]: #hasanyvalue

[94]: #parameters-30

[95]: #examples-30

[96]: #hasnovalue

[97]: #parameters-31

[98]: #examples-31

[99]: #matchesselector

[100]: #parameters-32

[101]: #examples-32

[102]: #doesnotmatchselector

[103]: #parameters-33

[104]: #examples-33

[105]: #hastagname

[106]: #parameters-34

[107]: #examples-34

[108]: #doesnothavetagname

[109]: #parameters-35

[110]: #examples-35

[111]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String

[112]: https://developer.mozilla.org/en-US/docs/Web/HTML/Element

[113]: https://developer.mozilla.org/de/docs/Web/API/Document/querySelector

[114]: #doesNotExist

[115]: https://developer.mozilla.org/docs/Web/HTML/Element

[116]: https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Object

[117]: https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Number

[118]: https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String

[119]: #isNotChecked

[120]: #isChecked

[121]: #isNotFocused

[122]: #isFocused

[123]: #isNotRequired

[124]: #isRequired

[125]: #isValid

[126]: #isNotVisible

[127]: #isVisible

[128]: #doesNotHaveAttribute

[129]: https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/RegExp

[130]: #hasAttribute

[131]: #hasNoAria

[132]: #hasAria

[133]: #doesNotHaveProperty

[134]: #isNotDisabled

[135]: #isDisabled

[136]: #doesNotHaveClass

[137]: https://developer.mozilla.org/en-US/docs/Web/API/Element/classList

[138]: #hasClass

[139]: https://developer.mozilla.org/en-US/docs/Web/API/Window/getComputedStyle

[140]: #includesText

[141]: https://developer.mozilla.org/en-US/docs/Web/API/Node/textContent

[142]: #hasText

[143]: #hasNoText

[144]: #hasAnyValue

[145]: #hasNoValue

[146]: https://developer.mozilla.org/docs/Web/API/HTMLInputElement

[147]: #hasValue

[148]: https://developer.mozilla.org/en-US/docs/Web/API/Element/tagName
