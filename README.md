# ICOR-collected

If you saw `ICOR-collected/1` in your server logs, this page explains it.

## What it is

ICOR-collected is the "Keep a copy" feature of a personal notes app. When someone saves a link to one of your pages in their notes, the app can fetch that one page and keep a copy of its title, preview picture and readable text. The copy is kept in that person's own copy of the app; there is no central service.

## What it does

- Fetches only links a person has saved: automatically when they save the link (they can switch this off), or when they press "Keep a copy".
- Makes one or two requests per copy: the page, and its preview picture if the page names one. A direct PDF or image link is a single request.
- Fetches HTTPS links on the standard port only, and refuses private, local and reserved network addresses.
- Follows up to three redirects, and stops after 10 seconds per request and 30 seconds per copy.
- Stops reading when a response passes its size limit (2 MB for a page).
- Does not retry when a site answers 429 or refuses the request.
- Allows a manual re-fetch of the same item at most once a minute.

## What it does not do

- It does not follow links on your page or crawl your site.
- It does not run scripts or send cookies or logins.
- It does not publish or share the copy.

## Contact

To report a problem or ask a question about it, open an issue in this repository.
