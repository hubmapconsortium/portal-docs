# portal-docs
Markdown documentation to be displayed in the Portal. The mapping is simple: `.md` files here are served under `/docs` on the Portal. For example,
[`faq.md`](https://github.com/hubmapconsortium/portal-docs/blob/master/faq.md) in this repo
corresponds to [`/docs/faq`](https://portal.hubmapconsortium.org/docs/faq) in the Portal. 



This repo is included as a git submodule in [`portal-ui`](https://github.com/hubmapconsortium/portal-ui):
The documents are included in the JS bundle for the HuBMAP Portal, and rendered on the client-side.

Release schedule:
- Changes made by Monday 5pm will be 
  - deployed to DEV/TEST/STAGE Wednesday after 5pm,
  - and, if QA passes, on production by Thursday afternoon.
- Changes made by Wednesday 5pm will be 
  - deployed to DEV/TEST/STAGE Monday after 5pm,
  - and, if QA passes, on production by Tuesday afternoon.

This is the regular schedule: If something needs to be out faster, we can try to make it happen;
Conversely, sometimes there are problems with other systems which block release to production.

Chris Briggs (Harvard) oversees curation, assay, and metadata related topics and questions.

Melissa Schwenk (University of Pittsburgh) oversees general consortium and FAQ related topics and questions.

## **This shouldn't be where you read the docs!**

If you're here to read documentation, use [the Portal](https://portal.hubmapconsortium.org/docs/) instead!

This repo is mirrored there, and in that context, the URLS don't include `.md`.
As a consequence, links between documents in here in Github won't work. Besides that, the docs also reference other portions of the site that aren't in this repo at all.
