This paperclip plugin provides cross-browser support for the `placeholder` attribute. It's supported in all major browsers including IE8+.

## Installation

- `bower install paperclip-placeholder-pollyfill`

### Usage

You'll need to first register the pollyfill as a paperclip plugin:

```javascript
var paperclip = require("paperclip");

//note that the pollyfill isn't registered if the browser supports placeholder.
paperclip.use(require("paperclip-placeholder-pollyfill"));
```


After you've registered the placeholder pollyfill, you can start using it. For example:

hello.pc

```html
<!-- *placeholder* pollyfill is added for IE, and ignored for any other browser that supports it-->
<input type="text" placeholder="Enter name here" data-bind="{{ model: name }}" /> 

{{#if:name}}
  Hello {{name}}!
{{/}}
```

Would render properly in all browsers that don't support `placeholder`.
