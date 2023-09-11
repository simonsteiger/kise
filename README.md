# Karolinska Institutet Format

## Installing

*TODO*: Replace the `<github-organization>` with your GitHub organization.

```bash
quarto use template <github-organization>/<%= filesafename %>
```

This will install the extension and create an example qmd file that you can use as a starting place for your article.

## Using

*TODO*: Describe how to use your format.

## Format Options

*TODO*: If your format has options that can be set via document metadata, describe them.

Have to explore if below chunk can be included via metadata. Has no effect when included in `_extension.yml`.

Use this to remove small logo from title page:
``` js
include-after: |
  <script type="text/javascript">
    Reveal.on('ready', event => {
      if (event.indexh === 0) {
        document.querySelector("div.has-logo > img.slide-logo").style.display = "none";
      }
    });
    Reveal.addEventListener('slidechanged', (event) => {
      if (event.indexh === 0) {
        Reveal.configure({ slideNumber: null });
        document.querySelector("div.has-logo > img.slide-logo").style.display = "none";
      }
      if (event.indexh === 1) { 
        Reveal.configure({ slideNumber: 'c' });
        document.querySelector("div.has-logo > img.slide-logo").style.display = null;
      }
    });
  </script>
```

## Example

Here is the source code for a minimal sample document: [example.qmd](example.qmd).
