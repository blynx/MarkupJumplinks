# MarkupJumplinks

ProcessWire module.

Helper for jumplink navigation creation.
Will create urls like `/url/to/page-name/#1023-page-name` from a given page or given title and url.

### Adds following Hooks

property hooks for $page:

`Page::anchorId`       returns 1023-page-name
`Page::anchorHref`     returns #1023-page-name
`Page::anchorUrlHref`  returns /url/to/page-name/#1023-page-name

### Methods

`::add($page_OR_title, $url = null)`

add an item to the storage.
If adding a page, override its url by providing another.

`::addAndGetId($page_OR_title, $url = null)`

add an item to the storage and immediately return an 'achorId' like "1023-title-name".

`::getAnchorId`

return something like "1023-title-name".

`::getAnchorHref`

return something like "#1023-title-name".

`::getAnchorUrlHref`

return something like "/url/to/page-name/#1023-title-name".

`::getArray`

get all stored items in an array of WireData objects

`::___renderAnchorTags(string $template)`

render all items as Markup. Provide a string with {\_href\_} and {\_content\_} as template.
Default: `<a href="{_href_}">{_content_}\</a>


### Todo


### Changelog

#### [0.0.1] - 2017-02-24

- Initial Release
